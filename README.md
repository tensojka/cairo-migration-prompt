# Prompt for LLMs to migrate Cairo 0 to Cairo 1

## How to use:

First put in the preamble, it should respond and summarize how it understands the differences. This helps it with the migrations later down the line and avoids a hidden limit on prompt length.

Then put in your Cairo 0 code wrapped in \<c0\> YOUR CODE HERE \</c0\> \<c1\>

Then it will understand that it should migrate the code. It doesn't understand anything about Cairo, always call the languages in c0 and c1. Using the word Cairo makes it confused as it knows some of Cairo's prehistoric 2021 syntax.

## Where to use:

Either ChatGPT Plus or [nat.dev](https://nat.dev) , where you can pay $5 to get easy access to gpt-4 and claude-v1, both of which are very good at this.
