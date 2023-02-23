---
title: PlainTextDocument.PlainTextDocument
linktitle: PlainTextDocument
second_title: Aspose.Words for .NET API Reference
description: PlainTextDocument constructor. Creates a plain text document from a file. Automatically detects the file format in C#.
type: docs
weight: 10
url: /net/aspose.words/plaintextdocument/plaintextdocument/
---
## PlainTextDocument(string) {#constructor_2}

Creates a plain text document from a file. Automatically detects the file format.

```csharp
public PlainTextDocument(string fileName)
```

| Parameter | Type | Description |
| --- | --- | --- |
| fileName | String | Name of the file to extract the text from. |

### Exceptions

| exception | condition |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | The document format is not recognized or not supported. |
| [FileCorruptedException](../../filecorruptedexception/) | The document appears to be corrupted and cannot be loaded. |
| Exception | There is a problem with the document and it should be reported to Aspose.Words developers. |
| IOException | There is an input/output exception. |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | The document is encrypted and requires a password to open, but you supplied an incorrect password. |
| ArgumentException | The name of the file cannot be null or empty string. |

## Examples

Shows how to load the contents of a Microsoft Word document in plaintext.

```csharp
Document doc = new Document(); 
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

doc.Save(ArtifactsDir + "PlainTextDocument.Load.docx");

PlainTextDocument plaintext = new PlainTextDocument(ArtifactsDir + "PlainTextDocument.Load.docx");

Assert.AreEqual("Hello world!", plaintext.Text.Trim());
```

### See Also

* class [PlainTextDocument](../)
* namespace [Aspose.Words](../../plaintextdocument/)
* assembly [Aspose.Words](../../../)

---

## PlainTextDocument(string, LoadOptions) {#constructor_3}

Creates a plain text document from a file. Allows to specify additional options such as an encryption password.

```csharp
public PlainTextDocument(string fileName, LoadOptions loadOptions)
```

| Parameter | Type | Description |
| --- | --- | --- |
| fileName | String | Name of the file to extract the text from. |
| loadOptions | LoadOptions | Additional options to use when loading a document. Can be `null`. |

### Exceptions

| exception | condition |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | The document format is not recognized or not supported. |
| [FileCorruptedException](../../filecorruptedexception/) | The document appears to be corrupted and cannot be loaded. |
| Exception | There is a problem with the document and it should be reported to Aspose.Words developers. |
| IOException | There is an input/output exception. |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | The document is encrypted and requires a password to open, but you supplied an incorrect password. |
| ArgumentException | The name of the file cannot be null or empty string. |

## Examples

Shows how to load the contents of an encrypted Microsoft Word document in plaintext.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
saveOptions.Password = "MyPassword";

doc.Save(ArtifactsDir + "PlainTextDocument.LoadEncrypted.docx", saveOptions);

LoadOptions loadOptions = new LoadOptions();
loadOptions.Password = "MyPassword";

PlainTextDocument plaintext = new PlainTextDocument(ArtifactsDir + "PlainTextDocument.LoadEncrypted.docx", loadOptions);

Assert.AreEqual("Hello world!", plaintext.Text.Trim());
```

### See Also

* class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* class [PlainTextDocument](../)
* namespace [Aspose.Words](../../plaintextdocument/)
* assembly [Aspose.Words](../../../)

---

## PlainTextDocument(Stream) {#constructor}

Creates a plain text document from a stream. Automatically detects the file format.

```csharp
public PlainTextDocument(Stream stream)
```

| Parameter | Type | Description |
| --- | --- | --- |
| stream | Stream | The stream where to extract the text from. |

### Exceptions

| exception | condition |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | The document format is not recognized or not supported. |
| [FileCorruptedException](../../filecorruptedexception/) | The document appears to be corrupted and cannot be loaded. |
| Exception | There is a problem with the document and it should be reported to Aspose.Words developers. |
| IOException | There is an input/output exception. |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | The document is encrypted and requires a password to open, but you supplied an incorrect password. |
| ArgumentNullException | The stream cannot be null. |
| NotSupportedException | The stream does not support reading or seeking. |
| ObjectDisposedException | The stream is a disposed object. |

## Remarks

The document must be stored at the beginning of the stream. The stream must support random positioning.

## Examples

Shows how to load the contents of a Microsoft Word document in plaintext using stream.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");
doc.Save(ArtifactsDir + "PlainTextDocument.LoadFromStream.docx");

using (FileStream stream = new FileStream(ArtifactsDir + "PlainTextDocument.LoadFromStream.docx", FileMode.Open))
{
    PlainTextDocument plaintext = new PlainTextDocument(stream);

    Assert.AreEqual("Hello world!", plaintext.Text.Trim());
}
```

### See Also

* class [PlainTextDocument](../)
* namespace [Aspose.Words](../../plaintextdocument/)
* assembly [Aspose.Words](../../../)

---

## PlainTextDocument(Stream, LoadOptions) {#constructor_1}

Creates a plain text document from a stream. Allows to specify additional options such as an encryption password.

```csharp
public PlainTextDocument(Stream stream, LoadOptions loadOptions)
```

| Parameter | Type | Description |
| --- | --- | --- |
| stream | Stream | The stream where to extract the text from. |
| loadOptions | LoadOptions | Additional options to use when loading a document. Can be `null`. |

### Exceptions

| exception | condition |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | The document format is not recognized or not supported. |
| [FileCorruptedException](../../filecorruptedexception/) | The document appears to be corrupted and cannot be loaded. |
| Exception | There is a problem with the document and it should be reported to Aspose.Words developers. |
| IOException | There is an input/output exception. |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | The document is encrypted and requires a password to open, but you supplied an incorrect password. |
| ArgumentNullException | The stream cannot be null. |
| NotSupportedException | The stream does not support reading or seeking. |
| ObjectDisposedException | The stream is a disposed object. |

## Remarks

The document must be stored at the beginning of the stream. The stream must support random positioning.

## Examples

Shows how to load the contents of an encrypted Microsoft Word document in plaintext using stream.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
saveOptions.Password = "MyPassword";

doc.Save(ArtifactsDir + "PlainTextDocument.LoadFromStreamWithOptions.docx", saveOptions);

LoadOptions loadOptions = new LoadOptions();
loadOptions.Password = "MyPassword";

using (FileStream stream = new FileStream(ArtifactsDir + "PlainTextDocument.LoadFromStreamWithOptions.docx", FileMode.Open))
{
    PlainTextDocument plaintext = new PlainTextDocument(stream, loadOptions);

    Assert.AreEqual("Hello world!", plaintext.Text.Trim());
}
```

### See Also

* class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* class [PlainTextDocument](../)
* namespace [Aspose.Words](../../plaintextdocument/)
* assembly [Aspose.Words](../../../)
