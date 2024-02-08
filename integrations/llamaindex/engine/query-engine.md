# Query Engine

A query engine serves as an end-to-end pipeline enabling users to ask questions about their data. It receives a natural language query and furnishes a response, accompanied by relevant context information retrieved and passed to the LLM (Large Language Model).

<figure><img src="../../../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>

## Inputs

* Vector Store Retriever
* [Response Synthesizer](../response-synthesizer/)

## Parameters

| Name                    | Description                                                                                                                                               |
| ----------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Return Source Documents | To return citations/sources that were used to build up the response                                                                                       |
| System Message          | An instruction for LLM on how to answer query                                                                                                             |
| Chain Option            | Method on how to summarize, answer questions, and extract information from documents. Read [more](https://js.langchain.com/docs/modules/chains/document/) |

## Outputs

| Name                           | Description                   |
| ------------------------------ | ----------------------------- |
| ConversationalRetrievalQAChain | Final node to return response |