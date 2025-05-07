---
title: Document constructor
linktitle: Document constructor
articleTitle: Document constructor
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Document constructor"
type: docs
weight: 10
url: /nodejs-net/aspose.words/document/constructor/
---

## Document() {#default}

Creates a blank Word document.


```js
Document()
```

### Remarks

A blank document is retrieved from resources, and by default, the resulting document looks more like created by [MsWordVersion.Word2007](../../../aspose.words.settings/mswordversion/#Word2007).
This blank document contains a default fonts table, minimal default styles, and latent styles.

[CompatibilityOptions.optimizeFor()](../../../aspose.words.settings/compatibilityoptions/optimizeFor/#mswordversion) method can be used to optimize the document contents as well as default Aspose.Words behavior to a particular version of MS Word.

The document paper size is Letter by default. If you want to change page setup, use
[Section.pageSetup](../../section/pageSetup/).

After creation, you can use [DocumentBuilder](../../documentbuilder/) to add document content easily.




## Document(fileName) {#string}

Opens an existing document from a file. Automatically detects the file format.


```js
Document(fileName: string)
```

| Parameter | Type | Description |
| --- | --- | --- |
| fileName | string | File name of the document to open. |

### Exceptions

| exception | condition |
| --- | --- |
| RuntimeError (Proxy error(UnsupportedFileFormatException)) | The document format is not recognized or not supported. |
| RuntimeError (Proxy error(FileCorruptedException)) | The document appears to be corrupted and cannot be loaded. |
| RuntimeError (Proxy error(Exception)) | There is a problem with the document and it should be reported to Aspose.Words developers. |
| RuntimeError (Proxy error(IOException)) | There is an input/output exception. |
| RuntimeError (Proxy error(IncorrectPasswordException)) | The document is encrypted and requires a password to open, but you supplied an incorrect password. |
| RuntimeError (Proxy error(ArgumentException)) | The name of the file cannot be null or empty string. |

## Document(fileName, loadOptions) {#string_loadoptions}

Opens an existing document from a file. Allows to specify additional options such as an encryption password.


```js
Document(fileName: string, loadOptions: Aspose.Words.Loading.LoadOptions)
```

| Parameter | Type | Description |
| --- | --- | --- |
| fileName | string | File name of the document to open. |
| loadOptions | [LoadOptions](../../../aspose.words.loading/loadoptions/) | Additional options to use when loading a document. Can be ``null``. |

### Exceptions

| exception | condition |
| --- | --- |
| RuntimeError (Proxy error(UnsupportedFileFormatException)) | The document format is not recognized or not supported. |
| RuntimeError (Proxy error(FileCorruptedException)) | The document appears to be corrupted and cannot be loaded. |
| RuntimeError (Proxy error(Exception)) | There is a problem with the document and it should be reported to Aspose.Words developers. |
| RuntimeError (Proxy error(IOException)) | There is an input/output exception. |
| RuntimeError (Proxy error(IncorrectPasswordException)) | The document is encrypted and requires a password to open, but you supplied an incorrect password. |
| RuntimeError (Proxy error(ArgumentException)) | The name of the file cannot be null or empty string. |

## Document(stream) {#buffer}

Opens an existing document from a stream. Automatically detects the file format.


```js
Document(stream: Buffer)
```

| Parameter | Type | Description |
| --- | --- | --- |
| stream | Buffer | Stream where to load the document from. |

### Remarks

The document must be stored at the beginning of the stream. The stream must support random positioning.




### Exceptions

| exception | condition |
| --- | --- |
| RuntimeError (Proxy error(UnsupportedFileFormatException)) | The document format is not recognized or not supported. |
| RuntimeError (Proxy error(FileCorruptedException)) | The document appears to be corrupted and cannot be loaded. |
| RuntimeError (Proxy error(Exception)) | There is a problem with the document and it should be reported to Aspose.Words developers. |
| RuntimeError (Proxy error(IOException)) | There is an input/output exception. |
| RuntimeError (Proxy error(IncorrectPasswordException)) | The document is encrypted and requires a password to open, but you supplied an incorrect password. |
| RuntimeError (Proxy error(ArgumentNullException)) | The stream cannot be null. |
| RuntimeError (Proxy error(NotSupportedException)) | The stream does not support reading or seeking. |
| RuntimeError (Proxy error(ObjectDisposedException)) | The stream is a disposed object. |

## Document(stream, loadOptions) {#buffer_loadoptions}

Opens an existing document from a stream. Allows to specify additional options such as an encryption password.


```js
Document(stream: Buffer, loadOptions: Aspose.Words.Loading.LoadOptions)
```

| Parameter | Type | Description |
| --- | --- | --- |
| stream | Buffer | The stream where to load the document from. |
| loadOptions | [LoadOptions](../../../aspose.words.loading/loadoptions/) | Additional options to use when loading a document. Can be ``null``. |

### Remarks

The document must be stored at the beginning of the stream. The stream must support random positioning.




### Exceptions

| exception | condition |
| --- | --- |
| RuntimeError (Proxy error(UnsupportedFileFormatException)) | The document format is not recognized or not supported. |
| RuntimeError (Proxy error(FileCorruptedException)) | The document appears to be corrupted and cannot be loaded. |
| RuntimeError (Proxy error(Exception)) | There is a problem with the document and it should be reported to Aspose.Words developers. |
| RuntimeError (Proxy error(IOException)) | There is an input/output exception. |
| RuntimeError (Proxy error(IncorrectPasswordException)) | The document is encrypted and requires a password to open, but you supplied an incorrect password. |
| RuntimeError (Proxy error(ArgumentNullException)) | The stream cannot be null. |
| RuntimeError (Proxy error(NotSupportedException)) | The stream does not support reading or seeking. |
| RuntimeError (Proxy error(ObjectDisposedException)) | The stream is a disposed object. |

## See Also

* module [Aspose.Words](../../)
* class [Document](../)

