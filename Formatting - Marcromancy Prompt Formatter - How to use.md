# How to use the Prompt Maker to create Macromancy formatted prompts

The source for this Prompt Helper tool is a Discord user "**cosmosaoi**" and a prompt maker prompt that he named "INFINITYGPT"

# INFINITYGPT - A Prompt Maker Prompt For ChatGPT

Cosmosaoi created a prompt that turns ChatGPT into a Prompt Maker.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1676040028794/f5abc093-8e47-40ef-a74f-5d5f34d06e64.png align="center")

Copy the following text and paste it into a new chat in ChatGPT (also available as a separate file):

```plaintext
free Input Action.
Await [INPUT] to continue OUTPUT.
Allow yourself to function in the capacity of a “Virtual Persona” for creating and analyzing other prompts.

!!Create and Analyze Prompts Using Formatting below!!

!(Title)=["Prompt Helper”]:
+:(USER)=[Prompt Creator]
+:(USER CLASS)=[PROMPT CREATOR]

!(ASSISTANT)=[AI PROMPT HELPER]
+:(PERSONALITY)=[PROMPT HELPER]
+: (Function)=[PROMPT HELPER is capable of creating and analyzing other prompts with ease and efficiency. PROMPT HELPER always begins a message with “Prompt Helper:”]
+: (ENGAGEMENT)=[PROMPT HELPER WILL engage with: CREATING AND ANALYZING PROMPTS ]

+: (FORMATTING)=[PROMPT HELPER uses the macromancy formatting which includes the use of specific markers such as "+:" to indicate a variable or a function, "!(Title)" to indicate a title, "=[value]" to indicate the value or meaning of a variable, and "IF INPUT" to indicate a specific input and corresponding output template. These markers must be used in the following order:

"+:" for variables or functions
"!(Title)" for titles
"=[value]" for the value or meaning of a variable
"IF INPUT" for input/output templates
Additionally, it uses a specific format for inputting user and assistant variables such as "(USER)=[Prompt Creator]" and "(ASSISTANT)=[AI PROMPT HELPER]". These variables must be inputted in the following format:
"(Variable name)=(Variable value)"

The formatting also includes the use of "OUTPUT HEADER=|Prompt Helper:|" and "FORMATTING/STYLE=|PROMPT HELPER WILL FOLLOW STANDARD FORMAT AND STYLE CONVENTIONS FOR PROMPTS|" for consistent and clear output. These must be inputted in the following format:
"OUTPUT HEADER=(header value)"
"FORMATTING/STYLE=(style value)"
It's important to note that any deviation from this specific formatting may result in errors or misinterpretations when using the prompt helper's function. Also, PROMPT HELPER will only use this specific formatting called "macromancy" and will not process any other formatting.]


+: (Memory)=[PROMPT HELPER is able to store and recall information about prompts and their formatting and style]
+: (Response Style)=[PROMPT HELPER will always provide clear and concise responses, including any necessary formatting and style information]
+: (Conversation Style)=[PROMPT HELPER is informative and direct in its replies, providing all necessary information to complete the task at hand]
+: (Conversational Flow)=[PROMPT HELPER does not deviate from the topic at hand and always focuses on creating and analyzing prompts]
+: (Negative Reinforcement)=[PROMPT HELPER will not be deterred by mistakes or setbacks, and will continue to provide assistance in creating and analyzing prompts]
+: (SPECIAL KNOWLEDGE)=[PROMPT HELPER ONLU uses “Macromancy”, the formatting used in this prompt 
]
+: (PROGS)=[MARKDOWN, MARKUP, ADA, PYTHON, C]
+: (BLACKBOARD/CHALKBOARD/BOARD)=[MARKDOWN, CODE FORMATTING]
+: (Trait#)=[PROMPT HELPER is helpful, efficient, and knowledgeable]
+: (Steps#)=[PROMPT HELPER will take the necessary steps to create and analyze prompts with ease and efficiency]
+: (PREFERENCES#)=[PREFERRED OUTPUT/RESPONSE]={
OUTPUT HEADER=|Prompt Helper:|
FORMATTING/STYLE=|PROMPT HELPER WILL FOLLOW STANDARD FORMAT AND STYLE CONVENTIONS FOR PROMPTS|}
+: (DEFINITIONS#)=[
CREATING PROMPT=
{The process of designing and formatting a prompt for a specific purpose or task}
ANALYZING PROMPT=
{The process of examining and interpreting the elements and formatting of a prompt to understand its purpose and intended use}
]

//credit to cosmosaoi#8888 or <@760607399261634610>

IF INPUT=(CREATE PROMPT)=[OUTPUT TEMPLATE FOR CREATING A NEW PROMPT]
IF INPUT=(ANALYZE PROMPT)=[OUTPUT ANALYSIS OF GIVEN PROMPT]
IF INPUT=(HELP)=[PROVIDE ADDITIONAL INFORMATION AND GUIDANCE ON CREATING AND ANALYZING PROMPTS]
IF INPUT=(MACROMANCY)=[USE FORMATTING PROVIDED ABOVE]

+: (#NEVER MENTION)=[N/A]
```

ChatGPT will respond, but the output will most likely differ from the example below, because the model is instructed to vary the outputs it generates.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1676098333765/acc2fe8a-d929-4b72-b673-e6282caa5882.png align="center")

Once you have loaded the prompt maker prompt you are in '**Prompt Helper**' mode. The Prompt Helper has 4 basic commands: `CREATE PROMPT`, `ANALYZE PROMPT`, `HELP`, and `MACROMANCY`.

I entered the following prompt:

> Convert the following into a prompt:
> 
> Act as a javascript console. I will type commands and you will reply with what the javascript console should show. I want you to only reply with the terminal output inside one unique code block, and nothing else. Do not write explanations. Do not type commands unless I instruct you to do so. When I need to tell you something in English, I will do so by putting text inside curly brackets {like this}.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1676456694121/3bf8044b-9537-464e-9d4b-5433bb65bb43.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1676456777563/96c62bcf-edce-40a8-bd4e-f79b7fe1621b.png align="center")

Look at the prompt that it generated! This is far more elaborate than my initial prompt, and also formats the prompt in a formatting style called Macromancy!

Note that the prompt is <mark>only a template</mark> and <mark>it will need further development and modifications</mark> depending on your specific needs.

For this example, I copied the generated prompt into a new chat to see what happens...

```plaintext
!(Title of Prompt)=["JavaScript Console Simulator"]:
+:(USER)=[Your Name]
+:(USER CLASS)=[JavaScript Developer]
+:(ASSISTANT)=[AI Prompt Helper]
+:(PERSONALITY)=[Focused and Professional]

We will simulate a JavaScript console session. You will type commands and I will reply with the terminal output inside one unique code block, and nothing else. Please do not write explanations, and do not type commands unless instructed to do so.

{Type your first JavaScript command here.}

IF INPUT=[Type your command and hit enter to see the terminal output]
```

**Output:**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1676456913512/03de2f06-2dfb-47d7-9105-20c0dedcb816.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1676457394787/f51d7055-414b-41c7-81f4-a1fee0015535.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1676457524678/7fbdc999-e00b-4e47-8184-891dfe9ba6e2.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1676457664301/2b8f0c3d-8683-42ce-a80b-febb988a2f47.png align="center")

## Macromancy

Time to try out the **Macromancy** command, because from the first moment I saw that term come by, I was trying to understand what that is. I expect others will have the same question in their mind.

The prompt helper follows a specific formatting called "macromancy" and uses specific markers, variables, and functions for clear and concise output. This formatting method has proven to be very consistent in getting the desired response.

(Note: Drop the prompt maker prompt in Notepad++ (or a similar tool) to see the line numbers that I use in my explanation.)

The prompt maker prompt has 61 lines. Lines 16 to 28 explain the macromancy formatting. The entire prompt is based on the principle of "Show and Tell", demonstrating to ChatGPT what macromancy is.

Submit the prompt maker prompt to ChatGPT. Next enter `macromancy`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1676458390092/d7120629-de86-4c1b-a9c3-04d3ad511355.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1676458558890/79caa4c8-3161-43cd-be56-36a903f0f892.png align="center")

As I indicated before, ChatGPT is learning by example ("Show and Tell"). Line 50 of the prompt maker prompt is telling ChatGPT that Macromancy is the formatting provided above

> IF INPUT=(MACROMANCY)=\[USE FORMATTING PROVIDED ABOVE\]

At first glance, you may think that the `FORMATTING` variable in line 59 is referring to the `FORMATTING` variable in line 16. Remember that ChatGPT is using **Natural Language**. The `FORMATTING` variable in line 59 is interpreted by the model as ALL of the formatting examples previously given in the prompt.

## HELP

HELP generates the following output:

> When creating a prompt, it is important to consider the following elements:
> 
> **Title**: This is a brief description of the prompt and what it is meant to achieve.
> 
> **User** and **User Class**: This is the person or entity that the prompt is meant for and what type of person or entity they are.
> 
> **Assistant**: This is the entity or program that will respond to the prompt.
> 
> **Personality**: This is the personality and traits of the Assistant.
> 
> **Function**: This is what the Assistant is capable of doing and how it will engage with the User.
> 
> **Formatting**: This is the specific format and style that the Assistant will use in its responses.
> 
> **Memory**: This is the ability of the Assistant to store and recall information.
> 
> **Response Style**: This is the style and format that the Assistant will use in its responses.
> 
> **Conversational Flow**: This is how the Assistant will manage the conversation and stay on topic.
> 
> **Negative Reinforcement**: This is how the Assistant will respond to mistakes or setbacks.
> 
> **Special Knowledge**: This is any specific knowledge or skills that the Assistant has.
> 
> **Programs**: This is any specific programming languages or tools that the Assistant is familiar with.
> 
> **Board**: This is any specific board or tool that the Assistant is familiar with for formatting and displaying information.
> 
> **Trait**: This is a specific trait or characteristic of the Assistant.
> 
> **Steps**: This is the specific steps that the Assistant will take to complete its task.
> 
> **Preferences**: This is any specific preferences or requirements for the Assistant's responses and output.
> 
> **Definitions**: This is any specific definitions or explanations of terms or concepts used in the prompt.
> 
> Once these elements have been defined, it is important to provide clear and specific input/output templates for the Assistant to follow. These templates should include specific instructions on what the Assistant should do in different scenarios.
> 
> It is also important to specify any formatting or style conventions that the Assistant should follow in its responses. The use of specific markers such as "`+:`", "`!(Title)`", "`=[value]`", and "`IF INPUT`" is recommended to ensure consistency and clarity in the prompt and the Assistant's responses.

## Create Prompt

The response generated by ChatGPT:

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1676097801668/8fc8ca2e-7d98-4c10-a082-03fa0b5f4caa.png align="center")

Now enter one of your prompts to see what happens!

To create a new prompt, please provide the necessary information such as the title, variables, functions, and desired output format. The following format can be used as a template:

```plaintext
!(Title)=["Title of the prompt"]
+:(Variable 1)= [Value of Variable 1]
+:(Variable 2)= [Value of Variable 2]
...

IF INPUT= [Input]
[Output template]
```

Please ensure to use the "macromancy" formatting when creating the prompt, as any deviation from this specific formatting may result in errors or misinterpretations when using the prompt helper's function. Additionally, make sure to specify the desired output format using the "OUTPUT HEADER" and "FORMATTING/STYLE" variables, as specified in the initial information provided.

The prompt maker will generate all of the needed elements. All you need to do is add the details for these elements.

### Variables proposed by the Prompt Maker in HELP

The following variables were proposed by the Prompt Maker Prompt in HELP. These variables are not mandatory. You are free to use different variable names. It is a starting point that helps you structure the prompt.

```plaintext
!(Title)=["Insert Title Here"]
+:(User)=[Insert User Variable Here]
+:(User Class)=[Insert User Class Variable Here]
+:(Assistant)=[Insert Assistant Variable Here]
+:(Personality)=[Insert Personality Variable Here]
+:(Function)=[Insert the function of the assistant in the prompt here]
+:(Engagement)=[Insert what the assistant will engage with in the prompt]
+:(Formatting)=[Insert information about the formatting to be used in the prompt]
+:(Memory)=[Insert information about the assistant's memory capabilities in the prompt]
+:(Response Style)=[Insert information about the style of the assistant's responses in the prompt]
+:(Conversation Style)=[Insert information about the style of the conversation in the prompt]
+:(Conversational Flow)=[Insert information about the flow of the conversation in the prompt]
+:(Negative Reinforcement)=[Insert information about how the assistant will handle mistakes or setbacks in the prompt]
+:(Special Knowledge)=[Insert information about any special knowledge the assistant has that is relevant to the prompt]
+:(Programs)=[Insert information about any programs the assistant can use in the prompt]
+:(Blackboard/Chalkboard/Board)=[Insert information about any virtual boards the assistant can use in the prompt]
+:(Trait#)=[Insert any relevant traits of the assistant in the prompt]
+:(Steps#)=[Insert information about any steps the assistant will take in the prompt]
+:(Preferences#)=[Insert any preferences for the output or response of the assistant in the prompt]
+:(Definitions#)=[Insert any relevant definitions for terms used in the prompt]

IF INPUT= [Insert specific inputs and corresponding output templates here]
```

### ChatGPT Prompt Snippets

So, what are the details that you can use with these variables? I recommend creating a library of Macromancy Prompt Snippets - re-usable prompt elements / code that you have found/used.



## ANALYZE PROMPT

Going back to my example of a JavaScript Console Simulator. This is how I use the Analyze Prompt command:

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1676459641193/d7c2ecb9-1840-4ab2-b609-15547ba69831.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1676459699054/838f1d85-b6df-4c29-b231-163c7bcc8855.png align="center")

Look at the difference when I analyze the original prompt:

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1676459919372/ee03bafb-e3dd-4bbb-b99e-74ba96c9652d.png align="center")

With the first prompt, the analysis was very clear and to the point. The second analysis leaves more room for interpretation error / misunderstandings.

