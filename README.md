# Prompt for LLMs to migrate Cairo 0 to Cairo 1

## How to use:

First put in `preamble.txt`, it should respond and summarize how it understands the differences. This helps it with the migrations later down the line and avoids a hidden limit on message length that is present in ChatGPT.

Then put in your Cairo 0 code like this:

`Now rewrite FUNCTION_NAME (below) to c1. No talk; just go.
<c0> YOUR CODE HERE </c0><c1>`

Then it will better that it should migrate the code, sometimes it tries to summarize it, this is due to the heavy instruction tuning. The nat.dev interface (below) is a bit better for this (you can leave out the 'Now rewrite..' bit) as it doesn't contain the system prompt 'You are ChatGPT, a helpful assistant yada yada'.

It doesn't understand anything about Cairo, always call the languages in c0 and c1. Using the word Cairo makes it confused as it knows some of Cairo's prehistoric 2021 syntax.

## Where to use:

Either ChatGPT Plus or [nat.dev](https://nat.dev) , where you can pay $5 to get easy access to gpt-4 and claude-v1, both of which are very good at this.
