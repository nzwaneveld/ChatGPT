# Effective prompt formats
The Prompt Helper is a great tool, but there can be several reasons why you would prefer to engineer your prompt in another manner. This chapter looks at the best practices that I came across while going through numerous groups, videos, etc. Due to the way the instruction-following models are trained or the data they are trained on, there are specific prompt formats that work particularly well and align better with the tasks at hand.

Here are a number of prompt formats that work reliably well, but feel free to explore different formats, which may fit your task best.

Rules of Thumb and Examples Note: the `"{text input here}"` is a placeholder for actual text/context

# Put instructions at the beginning of the prompt and use ### or """ to separate the instruction and context

```
Summarize the text below as a bullet point list of the most important points.
Text: """ {text input here} """  
```
The OpenAI documentation refers to `###` and `"""` as a Stop Sequence.

Every prompt contains a stop sequence. If you don't provide a stop sequence, then `/n` acts as the stop sequence.

The rule of first putting instructions in the prompt and then the context is not a hard rule, as illustrated in the following example.

# Stop Sequence example using """
This is an example provided by OpenAI that to shows how GPT can be used to **explain a complicated piece of code.**

**The prompt:**
```
class Log:
    def __init__(self, path):
        dirname = os.path.dirname(path)
        os.makedirs(dirname, exist_ok=True)
        f = open(path, "a+")

        # Check that the file is newline-terminated
        size = os.path.getsize(path)
        if size > 0:
            f.seek(size - 1)
            end = f.read(1)
            if end != "\n":
                f.write("\n")
        self.f = f
        self.path = path

    def log(self, event):
        event["_event_id"] = str(uuid.uuid4())
        json.dump(event, self.f)
        self.f.write("\n")

    def state(self):
        state = {"complete": set(), "last": None}
        for line in open(self.path):
            event = json.loads(line)
            if event["type"] == "submit" and event["success"]:
                state["complete"].add(event["id"])
                state["last"] = event
        return state

"""
Here's what the above class is doing:
1.
```

` """ ` is the stop sequence in this example. This stop sequence acts as a separator between two sections, a section with the context and a section containing the instructions. I have already seen examples of prompts containing multiple separators (stop sequences).

Be as specific, descriptive, and detailed as possible about the desired context, outcome, length, format, style, etc.

```
Write a short inspiring poem about a sunrise, seen on the beach with calm waters in the style of {famous poet}
```

# Show and tell
The models respond better when shown specific format requirements. This also makes it easier to programmatically parse out multiple outputs reliably.
```
Extract the important entities mentioned in the text below. First extract all company names, then extract all people names, then extract specific topics which fit the content and finally extract general overarching themes

Desired format:
Company names: <comma_separated_list_of_company_names>
People names: -||-
Specific topics: -||-
General themes: -||-

Text: {text}
```
## Zero-shot, then few-shot
**Zero-shot:**
```
Extract keywords from the below text.

Text: {text}

Keywords:
```
## Few-shot - using a couple of examples:

```
Extract keywords from the corresponding texts below.

Text 1: Stripe provides APIs that web developers can use to integrate payment processing into their websites and mobile applications.
Keywords 1: Stripe, payment processing, APIs, web developers, websites, mobile applications
###
Text 2: OpenAI has trained cutting-edge language models that are very good at understanding and generating text. Our API provides access to these models and can be used to solve virtually any task that involves processing language.
Keywords 2: OpenAI, language models, text processing, API.
###
Text 3: {text}
Keywords 3:
```

This prompt provides two examples. Text 3 is where you provide your text, and leave Keywords 3 empty. The model will generate the keywords.

Note the use of a stop sequence between each example.

# Reduce “fluffy” and imprecise descriptions
The following description is less effective:
```
The description for this product should be fairly short, a few sentences only, and not too much more.
```

This description is better:
```
Use a 3 to 5 sentence paragraph to describe this product.
```

# Tell the model what to do instead of telling it what it should NOT do
Less effective:
```
The following is a conversation between an Agent and a Customer. DO NOT ASK USERNAME OR PASSWORD. DO NOT REPEAT.

Customer: I can’t log in to my account.

Agent:
```

Better:
```
The following is a conversation between an Agent and a Customer. The agent will attempt to diagnose the problem and suggest a solution, whilst refraining from asking any questions related to PII. Instead of asking for PII, such as username or password, refer the user to the help article www.samplewebsite.com/help/faq

Customer: I can’t log in to my account.

Agent:
```
# Code Generation Specific - Use “leading words” to nudge the model toward a particular pattern
Less effective
```
# Write a simple python function that
# 1. Ask me for a number in mile
# 2. It converts miles to kilometers
In this code example below, adding “import” hints to the model that it should start writing in Python. (Similarly “SELECT” is a good hint for the start of a SQL statement.)
```
Better
```
# Write a simple python function that
# 1. Ask me for a number in mile
# 2. It converts miles to kilometers

import
```

# Markdown formatting
The ChatGPT web interface can render outputs using CommonMark. Not all Markdown formatting options are available, but some formatting can be implemented for various types of prompts.

One of the simplest examples is asking ChatGPT to output in a markdown table:
```
Create a markdown table listing 3 types of fruit, their color, and an interesting fact about each one

```

Other useful formatting options include:
```
# Heading 1
## Heading 2
### Heading 3

*italic text*, **bold text**, __underlined text__

[Hyperlinks](www.google.com)
![Images](https://image.pollinations.ai/prompt/lake)
```

See a more comprehensive formatting guide (with examples of each output type) in `ChatGPT Formatting Guide` [prompt]

## A comprehensive formatting guide for ChatGPT prompts using CommonMark
* **Line breaks**: To create a line break, simply press Enter/Return twice. Example: This is the first line. This is the second line.
* **Numbered lists**: To create a numbered list, start each item with a number and a period, followed by a space.
* **Bulleted lists**: To create a bulleted list, start each item with a dash (-) or an asterisk (*), followed by a space.
* **Bold text**: To format text in bold, surround the text with double asterisks (**).
* **Italic text**: To format text in italics, surround the text with single asterisks (*).
* **Bold and italic text**: To format text in both bold and italics, surround the text with triple asterisks (***).
* **Inline code**: To format text as inline code, surround the text with single backticks (`).
* **Code blocks**: To format multiple lines of code as a code block, surround the code with triple backticks (```), optionally followed by the name of the programming language.
* **Blockquotes**: To format text as a blockquote, start the text with a greater than sign (>), followed by a space. Example: > This is a blockquote.
* **URLs**: To include a URL in your prompt, simply paste the URL into the text.

# Multi-step prompting
ChatGPT has the ability to hold previous responses in memory, answer follow-up questions, or receive instructional inputs from the user. Here are some tips to make prompts involving multiple steps more consistent: - Specifying a "role" for ChatGPT is very effective. - It is often useful to specify the first output. - You may need to include explicit instructions against generating an input for the user. - Include clues for the model to keep track of its progress during a multi-step prompt, such as question numbers, countdowns or progress indicators.

Less effective
```
First ask me eight questions about my spending in various categories and then output a budget in a markdown table
```
Better
```
You are to act as a budget calculator whilst refraining from answering for the user. First, write "Question 1/8: How much do you earn per fortnight?". Wait for a response. Once you have received a response, ask a follow up question about the user's spending. Once all eight questions have been asked, create a markdown table with a sample budget for the user.
```

# Emphasizing Important Constraints
All throughout my research, I come across the tip that the best notation to use for engineering prompts for ChatGPT is using a bullet point list, as it clearly outlines the specific requirements for the prompt and makes it easier for the model to understand and follow.

The prompt in the previous example has bullet points, and clearly outlines the specific requirements for the prompt.

I recently discovered that using keywords such as "NEVER REPEAT" or "AVOID REPEATING" in **capital letters** helps emphasize the important constraints that must be followed.

In other words, present the prompt in a clear and effective way by using a combination of bullet points, sentence structure, and capitalized keywords to convey the requirements.
