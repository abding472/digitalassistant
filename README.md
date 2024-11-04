**What is this:**

Leverage OpenAI to interact with various documents on leadership, psychology, and cognitive science
In the data folder there are multiple markdown files.
Both documents are vectorized via OpenAI embedding and stored into Chroma.

**Technology leveraged**

> - Language: Python
> - Libraries: LangChain, OpenAI
> - VectorDB: Chroma
> - Embedding & LLM: OpenAI

**Setup:**

Make sure to install the requirements.txt file. The query uses OpenAI so you will need to retrieve your own key.
Store the API key as an environment variable.

**Running the Query:**

Run create_database.py first.

> python create_database.py

You can alter the chunk size & overlap to play with the number of documents needed
to aid the LLM. Currently default size and overlap set to 3000 & 600, respectively

When executing query_RAG.py model, the file leverages CLI prompting. For example

> python query_rag.py "How to increase standards of performance from the working team?"

Note you can adjust the K factor to request additional sources for contextual input when returning LLM output

**Additional Config (Optional):**

- Add additional markdown files
- Change the vector DB
- Change embedding & LLM solution
