---
title: PlainTextDocument constructor
linktitle: PlainTextDocument constructor
articleTitle: PlainTextDocument constructor
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.PlainTextDocument constructor"
type: docs
weight: 10
url: /nodejs-net/Aspose.Words/plaintextdocument/constructor/
---

## PlainTextDocument(fileName) {#string}

Creates a plain text document from a file. Automatically detects the file format.


```js
PlainTextDocument(fileName: string)
```

| Parameter | Type | Description |
| --- | --- | --- |
| fileName | string | Name of the file to extract the text from. |

### Exceptions

| exception | condition |
| --- | --- |
| RuntimeError (Proxy error(UnsupportedFileFormatException)) | The document format is not recognized or not supported. |
| RuntimeError (Proxy error(FileCorruptedException)) | The document appears to be corrupted and cannot be loaded. |
| RuntimeError (Proxy error(Exception)) | There is a problem with the document and it should be reported to Aspose.Words developers. |
| RuntimeError (Proxy error(IOException)) | There is an input/output exception. |
| RuntimeError (Proxy error(IncorrectPasswordException)) | The document is encrypted and requires a password to open, but you supplied an incorrect password. |
| RuntimeError (Proxy error(ArgumentException)) | The name of the file cannot be null or empty string. |

## PlainTextDocument(fileName, loadOptions) {#string_loadoptions}

Creates a plain text document from a file. Allows to specify additional options such as an encryption password.


```js
PlainTextDocument(fileName: stringloadOptions: Aspose.Words.Loading.LoadOptions)
```

| Parameter | Type | Description |
| --- | --- | --- |
| fileName | string | Name of the file to extract the text from. |
| loadOptions | [LoadOptions](../../../Aspose.Words.Loading/loadoptions/) | Additional options to use when loading a document. Can be ``None``. |

### Remarks




### Exceptions

| exception | condition |
| --- | --- |
| RuntimeError (Proxy error(UnsupportedFileFormatException)) | The document format is not recognized or not supported. |
| RuntimeError (Proxy error(FileCorruptedException)) | The document appears to be corrupted and cannot be loaded. |
| RuntimeError (Proxy error(Exception)) | There is a problem with the document and it should be reported to Aspose.Words developers. |
| RuntimeError (Proxy error(IOException)) | There is an input/output exception. |
| RuntimeError (Proxy error(IncorrectPasswordException)) | The document is encrypted and requires a password to open, but you supplied an incorrect password. |
| RuntimeError (Proxy error(ArgumentException)) | The name of the file cannot be null or empty string. |

## PlainTextDocument(stream) {#buffer}

Creates a plain text document from a stream. Automatically detects the file format.


```js
PlainTextDocument(stream: Buffer)
```

| Parameter | Type | Description |
| --- | --- | --- |
| stream | Buffer | The stream where to extract the text from. |

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

## PlainTextDocument(stream, loadOptions) {#buffer_loadoptions}

Creates a plain text document from a stream. Allows to specify additional options such as an encryption password.


```js
PlainTextDocument(stream: BufferloadOptions: Aspose.Words.Loading.LoadOptions)
```

| Parameter | Type | Description |
| --- | --- | --- |
| stream | Buffer | The stream where to extract the text from. |
| loadOptions | [LoadOptions](../../../Aspose.Words.Loading/loadoptions/) | Additional options to use when loading a document. Can be ``None``. |

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
* class [PlainTextDocument](../)

