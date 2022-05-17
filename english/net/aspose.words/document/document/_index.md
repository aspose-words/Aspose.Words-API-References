---
title: Document
second_title: Aspose.Words for .NET API Reference
description: 
type: docs
weight: 10
url: /net/aspose.words/document/document/
---
## Document constructor (1 of 5)

Creates a blank Word document.

```csharp
public Document()
```

### Remarks

The document paper size is Letter by default. If you want to change page setup, use [`Section.PageSetup`](../../section/pagesetup).

After creation, you can use [`DocumentBuilder`](../../documentbuilder) to add document content easily.

### See Also

* class [Document](../../document)
* namespace [Aspose.Words](../../document)
* assembly [Aspose.Words](../../../)

---

## Document constructor (2 of 5)

Opens an existing document from a file. Automatically detects the file format.

```csharp
public Document(string fileName)
```

| Parameter | Type | Description |
| --- | --- | --- |
| fileName | String | File name of the document to open. |

### Exceptions

| exception | condition |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception) | The document format is not recognized or not supported. |
| [FileCorruptedException](../../filecorruptedexception) | The document appears to be corrupted and cannot be loaded. |
| Exception | There is a problem with the document and it should be reported to Aspose.Words developers. |
| IOException | There is an input/output exception. |
| [IncorrectPasswordException](../../incorrectpasswordexception) | The document is encrypted and requires a password to open, but you supplied an incorrect password. |
| ArgumentException | The name of the file cannot be null or empty string. |

### See Also

* class [Document](../../document)
* namespace [Aspose.Words](../../document)
* assembly [Aspose.Words](../../../)

---

## Document constructor (3 of 5)

Opens an existing document from a file. Allows to specify additional options such as an encryption password.

```csharp
public Document(string fileName, LoadOptions loadOptions)
```

| Parameter | Type | Description |
| --- | --- | --- |
| fileName | String | File name of the document to open. |
| loadOptions | LoadOptions | Additional options to use when loading a document. Can be null. |

### Exceptions

| exception | condition |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception) | The document format is not recognized or not supported. |
| [FileCorruptedException](../../filecorruptedexception) | The document appears to be corrupted and cannot be loaded. |
| Exception | There is a problem with the document and it should be reported to Aspose.Words developers. |
| IOException | There is an input/output exception. |
| [IncorrectPasswordException](../../incorrectpasswordexception) | The document is encrypted and requires a password to open, but you supplied an incorrect password. |
| ArgumentException | The name of the file cannot be null or empty string. |

### See Also

* class [LoadOptions](../../../aspose.words.loading/loadoptions)
* class [Document](../../document)
* namespace [Aspose.Words](../../document)
* assembly [Aspose.Words](../../../)

---

## Document constructor (4 of 5)

Opens an existing document from a stream. Automatically detects the file format.

```csharp
public Document(Stream stream)
```

| Parameter | Type | Description |
| --- | --- | --- |
| stream | Stream | Stream where to load the document from. |

### Exceptions

| exception | condition |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception) | The document format is not recognized or not supported. |
| [FileCorruptedException](../../filecorruptedexception) | The document appears to be corrupted and cannot be loaded. |
| Exception | There is a problem with the document and it should be reported to Aspose.Words developers. |
| IOException | There is an input/output exception. |
| [IncorrectPasswordException](../../incorrectpasswordexception) | The document is encrypted and requires a password to open, but you supplied an incorrect password. |
| ArgumentNullException | The stream cannot be null. |
| NotSupportedException | The stream does not support reading or seeking. |
| ObjectDisposedException | The stream is a disposed object. |

### Remarks

The document must be stored at the beginning of the stream. The stream must support random positioning.

### See Also

* class [Document](../../document)
* namespace [Aspose.Words](../../document)
* assembly [Aspose.Words](../../../)

---

## Document constructor (5 of 5)

Opens an existing document from a stream. Allows to specify additional options such as an encryption password.

```csharp
public Document(Stream stream, LoadOptions loadOptions)
```

| Parameter | Type | Description |
| --- | --- | --- |
| stream | Stream | The stream where to load the document from. |
| loadOptions | LoadOptions | Additional options to use when loading a document. Can be null. |

### Exceptions

| exception | condition |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception) | The document format is not recognized or not supported. |
| [FileCorruptedException](../../filecorruptedexception) | The document appears to be corrupted and cannot be loaded. |
| Exception | There is a problem with the document and it should be reported to Aspose.Words developers. |
| IOException | There is an input/output exception. |
| [IncorrectPasswordException](../../incorrectpasswordexception) | The document is encrypted and requires a password to open, but you supplied an incorrect password. |
| ArgumentNullException | The stream cannot be null. |
| NotSupportedException | The stream does not support reading or seeking. |
| ObjectDisposedException | The stream is a disposed object. |

### Remarks

The document must be stored at the beginning of the stream. The stream must support random positioning.

### See Also

* class [LoadOptions](../../../aspose.words.loading/loadoptions)
* class [Document](../../document)
* namespace [Aspose.Words](../../document)
* assembly [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
