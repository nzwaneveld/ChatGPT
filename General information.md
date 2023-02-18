# Prompt size limitations
There is no clear limitation. The common length of a prompt is less than 256 tokens, but it can be higher, even up to 1024 tokens. (I have also seen a post by OpenAI indicating max 2000 words in a prompt.) Long prompts can be difficult for the model to understand and may even generate an inaccurate response. BUT, when you present the data in the prompt in a highly structured manner, you also reduce the risk that the model doesn't understand or generate undesired responses. Rule of thumb: “Less is more!”

## Tokens
The GPT family of models process text using tokens, which are common sequences of characters found in text. The models understand the statistical relationships between these tokens, and excel at producing the next token in a sequence of tokens. While studying the GPT API documentation, I came across an interesting tool provided by OpenAI called the Tokenizer (https://platform.openai.com/tokenizer). You can use this tool to understand how a piece of text would be tokenized by the API, and see the total count of tokens in that piece of text. It also shows you the token IDs.

**The key takeaways:**
* Many words map to one token, but some don't: indivisible.
* Unicode characters like emojis may be split into many tokens containing the underlying bytes: 🤚🏾
* A helpful rule of thumb is that one token generally corresponds to ~4 characters of text for common English text. This translates to roughly ¾ of a word (so 100 tokens ~= 75 words). If we take 1024 tokens as the maximum (based on comments I found in some of the API notes, that would translate roughly to 768 words.

We have already seen examples where use a prompt to instruct the model and then submit data in the next prompt for processing. We also know that the model 'remembers' the entire thread. This leads me to believe that we can split larger amounts of data into blocks smaller than 1024 tokens / approx. 768 words. (One of my next experiments will be to see if / how I can have the model process a transcript containing 5000+ words and extract all the action items.)

