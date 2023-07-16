# AMPCOMEGPT

# Environment Setup
first install all requirements:

```shell
pip3 install -r requirements.txt
```

Then, download the LLM model and place it in a model directory:
- LLM: default to [ggml-gpt4all-j-v1.3-groovy.bin](https://gpt4all.io/models/ggml-gpt4all-j-v1.3-groovy.bin). 


Note: because of the way `langchain` loads the `SentenceTransformers` embeddings, the first time it will requires internet connection to download the embeddings model itself.


## Instructions to ingest dataset

Add files to source documents folder

The supported extensions are:

   - `.csv`: CSV,
   - `.docx`: Word Document,
   - `.doc`: Word Document,
   - `.enex`: EverNote,
   - `.eml`: Email,
   - `.epub`: EPub,
   - `.html`: HTML File,
   - `.md`: Markdown,
   - `.msg`: Outlook Message,
   - `.odt`: Open Document Text,
   - `.pdf`: Portable Document Format (PDF),
   - `.pptx` : PowerPoint Document,
   - `.ppt` : PowerPoint Document,
   - `.txt`: Text file (UTF-8),

Run the following command to ingest all the data.

```shell
python ingest.py
```

Note: during the ingest process no data leaves local environment. 

## Ask questions with documents, locally using GPT4all!
Please put model=GPT4All in .env file
In order to ask a question, run a command like:

```shell
python ampcome_gpt.py
```

And can chat with it.

Type `exit` to finish the script.

## Ask questions to your documents, with API using PALM!
Please put model=Palm in .env file,
- added memory buffer.
- added some prompt engineering as well

In order to ask a question, run a command like:

```shell
python ampcome_gpt.py
```

And can chat with it.

Type `exit` to finish the script.




