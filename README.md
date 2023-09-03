Create a simple LLM with local model without any fancy stuff

This will init a LLM with the local model, which can be something like
the quantized model `llama-2-7b-chat.ggmlv3.q4_0.bin`.
Please note that the GGML quantization format is EOL since August 2023
and replaced by the GGUF format. Download the respective model or
stick with `llama-cpp-python=0.1.78`.

A template is setup, which is a system prompt to tell the LLM what it is.
This is here very basic and nothing special. This is transformed into
a PromptTemplate for reusability and passed with the LLM into a LLMChain.

This chain can be run, by using `llm_chain.run("question as string")`

For the question to the AI:

```What is the capitol of Germany, France and Brasil? ```

The result is printed and could look like this:

```
    The result of the AI is: ==>

    Germany: The capital of Germany is Berlin.

    France: The capital of France is Paris.

    Brasil (not a country): Brasil is not a country, it's the Portuguese name for Brazil. The capital of Brazil is Brasília.
    <== end of result
```

This is it for the first step.
