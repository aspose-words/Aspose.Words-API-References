---
title: DigitalSignatureUtil.LoadSignatures
linktitle: LoadSignatures
articleTitle: LoadSignatures
second_title: Aspose.Words for .NET
description: Effortlessly load digital signatures from your documents with the DigitalSignatureUtil LoadSignatures method. Enhance your workflow today!
type: docs
weight: 10
url: /net/aspose.words.digitalsignatures/digitalsignatureutil/loadsignatures/
---
## LoadSignatures(*string*) {#loadsignatures_1}

Loads digital signatures from document.

```csharp
public static DigitalSignatureCollection LoadSignatures(string fileName)
```

| Parameter | Type | Description |
| --- | --- | --- |
| fileName | String | Path to the document. |

### Return Value

Collection of digital signatures. Returns empty collection if file is not signed.

## Examples

Shows how to load signatures from a digitally signed document.

```csharp
// There are two ways of loading a signed document's collection of digital signatures using the DigitalSignatureUtil class.
// 1 -  Load from a document from a local file system filename:
DigitalSignatureCollection digitalSignatures = 
    DigitalSignatureUtil.LoadSignatures(MyDir + "Digitally signed.docx");

// If this collection is nonempty, then we can verify that the document is digitally signed.
Assert.That(digitalSignatures.Count, Is.EqualTo(1));

// 2 -  Load from a document from a FileStream:
using (Stream stream = new FileStream(MyDir + "Digitally signed.docx", FileMode.Open))
{
    digitalSignatures = DigitalSignatureUtil.LoadSignatures(stream);
    Assert.That(digitalSignatures.Count, Is.EqualTo(1));
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
Assert.That(DigitalSignatureUtil.LoadSignatures(ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromString.docx").Count, Is.EqualTo(0));
Assert.That(DigitalSignatureUtil.LoadSignatures(ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromStream.docx").Count, Is.EqualTo(0));
```

### See Also

* class [DigitalSignatureCollection](../../digitalsignaturecollection/)
* class [DigitalSignatureUtil](../)
* namespace [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* assembly [Aspose.Words](../../../)

---

## LoadSignatures(*Stream*) {#loadsignatures}

Loads digital signatures from document using stream.

```csharp
public static DigitalSignatureCollection LoadSignatures(Stream stream)
```

| Parameter | Type | Description |
| --- | --- | --- |
| stream | Stream | Stream with the document. |

### Return Value

Collection of digital signatures. Returns empty collection if file is not signed.

## Examples

Shows how to load signatures from a digitally signed document.

```csharp
// There are two ways of loading a signed document's collection of digital signatures using the DigitalSignatureUtil class.
// 1 -  Load from a document from a local file system filename:
DigitalSignatureCollection digitalSignatures = 
    DigitalSignatureUtil.LoadSignatures(MyDir + "Digitally signed.docx");

// If this collection is nonempty, then we can verify that the document is digitally signed.
Assert.That(digitalSignatures.Count, Is.EqualTo(1));

// 2 -  Load from a document from a FileStream:
using (Stream stream = new FileStream(MyDir + "Digitally signed.docx", FileMode.Open))
{
    digitalSignatures = DigitalSignatureUtil.LoadSignatures(stream);
    Assert.That(digitalSignatures.Count, Is.EqualTo(1));
}
```

### See Also

* class [DigitalSignatureCollection](../../digitalsignaturecollection/)
* class [DigitalSignatureUtil](../)
* namespace [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* assembly [Aspose.Words](../../../)
