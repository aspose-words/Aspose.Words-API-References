---
title: PlainTextDocument
second_title: Aspose.Words for .NET API Reference
description: 
type: docs
weight: 10
url: /net/aspose.words/plaintextdocument/plaintextdocument/
---
## PlainTextDocument constructor (1 of 4)

Creates a plain text document from a stream. Automatically detects the file format.

```csharp
public PlainTextDocument(Stream stream)
```

| parameter | description |
| --- | --- |
| stream | The stream where to extract the text from. |

## Exceptions

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

## Remarks

The document must be stored at the beginning of the stream. The stream must support random positioning.

### See Also

* class [PlainTextDocument](../../plaintextdocument)
* namespace [Aspose.Words](../../plaintextdocument)
* assembly [Aspose.Words](../../../)

---

## PlainTextDocument constructor (2 of 4)

Creates a plain text document from a file. Automatically detects the file format.

```csharp
public PlainTextDocument(string fileName)
```

| parameter | description |
| --- | --- |
| fileName | Name of the file to extract the text from. |

## Exceptions

| exception | condition |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception) | The document format is not recognized or not supported. |
| [FileCorruptedException](../../filecorruptedexception) | The document appears to be corrupted and cannot be loaded. |
| Exception | There is a problem with the document and it should be reported to Aspose.Words developers. |
| IOException | There is an input/output exception. |
| [IncorrectPasswordException](../../incorrectpasswordexception) | The document is encrypted and requires a password to open, but you supplied an incorrect password. |
| ArgumentException | The name of the file cannot be null or empty string. |

### See Also

* class [PlainTextDocument](../../plaintextdocument)
* namespace [Aspose.Words](../../plaintextdocument)
* assembly [Aspose.Words](../../../)

---

## PlainTextDocument constructor (3 of 4)

Creates a plain text document from a stream. Allows to specify additional options such as an encryption password.

```csharp
public PlainTextDocument(Stream stream, LoadOptions loadOptions)
```

| parameter | description |
| --- | --- |
| stream | The stream where to extract the text from. |
| loadOptions | Additional options to use when loading a document. Can be null. |

## Exceptions

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

## Remarks

The document must be stored at the beginning of the stream. The stream must support random positioning.

### See Also

* class [LoadOptions](../../../aspose.words.loading/loadoptions)
* class [PlainTextDocument](../../plaintextdocument)
* namespace [Aspose.Words](../../plaintextdocument)
* assembly [Aspose.Words](../../../)

---

## PlainTextDocument constructor (4 of 4)

Creates a plain text document from a file. Allows to specify additional options such as an encryption password.

```csharp
public PlainTextDocument(string fileName, LoadOptions loadOptions)
```

| parameter | description |
| --- | --- |
| fileName | Name of the file to extract the text from. |
| loadOptions | Additional options to use when loading a document. Can be null. |

## Exceptions

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
* class [PlainTextDocument](../../plaintextdocument)
* namespace [Aspose.Words](../../plaintextdocument)
* assembly [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
