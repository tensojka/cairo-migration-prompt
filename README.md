# Prompt for LLMs to migrate Cairo 0 to Cairo 1

## How to use:

First put in `preamble.txt`, it should respond and summarize how it understands the differences. This helps it with the migrations later down the line and avoids a hidden limit on message length (around 3000 tokens, if you go over the rest is just ignored) that is present in ChatGPT.

Then put in your Cairo 0 code like this:

`Rewrite code below to c1. No talk; just go.
<c0> YOUR CODE HERE </c0><c1>`

Then it will better understand that it should migrate the code, sometimes it tries to summarize it, this is due to the heavy instruction tuning. The nat.dev interface (below) is a bit better for this (you can leave out the 'Now rewrite..' bit) as it doesn't contain the system prompt 'You are ChatGPT, a helpful assistant yada yada'.

It doesn't understand anything about Cairo, always call the languages in c0 and c1. Using the word Cairo makes it confused as it knows some of Cairo's prehistoric 2021 syntax.

## Where to use:

Either ChatGPT Plus or [nat.dev](https://nat.dev), where you can pay $5 to get pay-as-you-go access to gpt-4 and claude-v1, both of which are very good at this.

## Limitations

The 4k context window of ChatGPT GPT-4 is really too low to explain c1. I want to use this mainly there, so I'm trying to stay under it. The code is good as a first draft, to save you from the manual work, but it almost never works on the first try. If you go over the token limit in ChatGPT, the output cuts off and you must say Continue or similar – but then, the model doesn't have access to the whole preamble. Thus it's better to edit your prompts in ChatGPT rather than converse with the model to save context.

GPT-4 on [nat.dev](https://nat.dev) has a 8k token context window.

## Development

You can check token counts at [tiktoken calculator](https://huggingface.co/spaces/JacobLinCool/tiktoken-calculator), I try to keep the preamble under 3k tokens.

Suggestions appreciated
