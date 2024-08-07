# What is UnstructuredDirectoryLoader?

- UnstructuredDirectoryLoader uses 🦜️🔗 LangChain <langchain_community.document_loaders.unstructured> **UnstructuredFileLoader** to load files like '.txt', '.csv', '.pdf', '.msg' into a List[Document] using  🦜️🔗 LangChain <langchain_core.documents> **Document**

## How to install

### Setup Python environment

The Python version used when this was developed was 3.9

```
pip install UnstructuredDirectoryLoader
```

### How to use

1. Just pass you local directory path in UnstructuredDirectoryLoader() and then use this directory loader.

    ```
    directory_loader = UnstructuredDirectoryLoader(directory_path='*<Your_Local_Folder_Path>*')
    ```

    ```
    listDocs = directory_loader.load()
    ```

3. Done! Go ahead and use a text splitter on this docs

    ```
    text_splitter = SemanticChunker(HuggingFaceEmbeddings())
    ```
