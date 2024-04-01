---
title: DigitalSignatureUtil Class
linktitle: DigitalSignatureUtil
articleTitle: DigitalSignatureUtil
second_title: Aspose.Words for .NET
description: Aspose.Words.DigitalSignatures.DigitalSignatureUtil class. Provides methods for signing document in C#.
type: docs
weight: 490
url: /net/aspose.words.digitalsignatures/digitalsignatureutil/
---
## DigitalSignatureUtil class

Provides methods for signing document.

To learn more, visit the [Work with Digital Signatures](https://docs.aspose.com/words/net/working-with-digital-signatures/) documentation article.

```csharp
public static class DigitalSignatureUtil
```

## Methods

| Name | Description |
| --- | --- |
| static [LoadSignatures](../../aspose.words.digitalsignatures/digitalsignatureutil/loadsignatures/#loadsignatures)(*Stream*) | Loads digital signatures from document using stream. |
| static [LoadSignatures](../../aspose.words.digitalsignatures/digitalsignatureutil/loadsignatures/#loadsignatures_1)(*string*) | Loads digital signatures from document. |
| static [RemoveAllSignatures](../../aspose.words.digitalsignatures/digitalsignatureutil/removeallsignatures/#removeallsignatures)(*Stream, Stream*) | Removes all digital signatures from document in source stream and writes unsigned document to destination stream. |
| static [RemoveAllSignatures](../../aspose.words.digitalsignatures/digitalsignatureutil/removeallsignatures/#removeallsignatures_1)(*string, string*) | Removes all digital signatures from source file and writes unsigned file to destination file. |
| static [Sign](../../aspose.words.digitalsignatures/digitalsignatureutil/sign/#sign)(*Stream, Stream, [CertificateHolder](../certificateholder/)*) | Signs source document using given [`CertificateHolder`](../certificateholder/) with digital signature and writes signed document to destination stream. |
| static [Sign](../../aspose.words.digitalsignatures/digitalsignatureutil/sign/#sign_2)(*string, string, [CertificateHolder](../certificateholder/)*) | Signs source document using given [`CertificateHolder`](../certificateholder/) with digital signature and writes signed document to destination file. |
| static [Sign](../../aspose.words.digitalsignatures/digitalsignatureutil/sign/#sign_1)(*Stream, Stream, [CertificateHolder](../certificateholder/), [SignOptions](../signoptions/)*) | Signs source document using given [`CertificateHolder`](../certificateholder/) and [`SignOptions`](../signoptions/) with digital signature and writes signed document to destination stream. |
| static [Sign](../../aspose.words.digitalsignatures/digitalsignatureutil/sign/#sign_3)(*string, string, [CertificateHolder](../certificateholder/), [SignOptions](../signoptions/)*) | Signs source document using given [`CertificateHolder`](../certificateholder/) and [`SignOptions`](../signoptions/) with digital signature and writes signed document to destination file. |

## Remarks

Since digital signature works with file content rather than Document Object Model these methods are put into a separate class.

Supported formats are: Doc, Dot, Docx, Dotx, Docm, Odt, Ott.

## Examples

Shows how to load signatures from a digitally signed document.

```csharp
// There are two ways of loading a signed document's collection of digital signatures using the DigitalSignatureUtil class.
// 1 -  Load from a document from a local file system filename:
DigitalSignatureCollection digitalSignatures = 
    DigitalSignatureUtil.LoadSignatures(MyDir + "Digitally signed.docx");

// If this collection is nonempty, then we can verify that the document is digitally signed.
Assert.AreEqual(1, digitalSignatures.Count);

// 2 -  Load from a document from a FileStream:
using (Stream stream = new FileStream(MyDir + "Digitally signed.docx", FileMode.Open))
{
    digitalSignatures = DigitalSignatureUtil.LoadSignatures(stream);
    Assert.AreEqual(1, digitalSignatures.Count);
}
```

Shows how to remove digital signatures from a digitally signed document.

```csharp
// There are two ways of using the DigitalSignatureUtil class to remove digital signatures
// from a signed document by saving an unsigned copy of it somewhere else in the local file system.
// 1 - Determine the locations of both the signed document and the unsigned copy by filename strings:
DigitalSignatureUtil.RemoveAllSignatures(MyDir + "Digitally signed.docx",
    ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromString.docx");

// 2 - Determine the locations of both the signed document and the unsigned copy by file streams:
using (Stream streamIn = new FileStream(MyDir + "Digitally signed.docx", FileMode.Open))
{
    using (Stream streamOut = new FileStream(ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromStream.docx", FileMode.Create))
    {
        DigitalSignatureUtil.RemoveAllSignatures(streamIn, streamOut);
    }
}

// Verify that both our output documents have no digital signatures.
Assert.AreEqual(0, DigitalSignatureUtil.LoadSignatures(ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromString.docx").Count);
Assert.AreEqual(0, DigitalSignatureUtil.LoadSignatures(ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromStream.docx").Count);
```

### See Also

* namespace [Aspose.Words.DigitalSignatures](../../aspose.words.digitalsignatures/)
* assembly [Aspose.Words](../../)
