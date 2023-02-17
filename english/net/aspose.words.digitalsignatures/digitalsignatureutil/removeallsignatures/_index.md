---
title: DigitalSignatureUtil.RemoveAllSignatures
second_title: Aspose.Words for .NET API Reference
description: DigitalSignatureUtil method. Removes all digital signatures from source file and writes unsigned file to destination file in C#.
type: docs
weight: 20
url: /net/aspose.words.digitalsignatures/digitalsignatureutil/removeallsignatures/
---
## RemoveAllSignatures(string, string) {#removeallsignatures_1}

Removes all digital signatures from source file and writes unsigned file to destination file.

```csharp
public static void RemoveAllSignatures(string srcFileName, string dstFileName)
```

## Examples

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
Assert.That(DigitalSignatureUtil.LoadSignatures(ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromString.docx"), Is.Empty);
Assert.That(DigitalSignatureUtil.LoadSignatures(ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromStream.docx"), Is.Empty);
```

### See Also

* class [DigitalSignatureUtil](../)
* namespace [Aspose.Words.DigitalSignatures](../../digitalsignatureutil/)
* assembly [Aspose.Words](../../../)

---

## RemoveAllSignatures(Stream, Stream) {#removeallsignatures}

Removes all digital signatures from document in source stream and writes unsigned document to destination stream.

**Output will be written to the start of stream and stream size will be updated with content length.**

```csharp
public static void RemoveAllSignatures(Stream srcStream, Stream dstStream)
```

## Examples

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
Assert.That(DigitalSignatureUtil.LoadSignatures(ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromString.docx"), Is.Empty);
Assert.That(DigitalSignatureUtil.LoadSignatures(ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromStream.docx"), Is.Empty);
```

### See Also

* class [DigitalSignatureUtil](../)
* namespace [Aspose.Words.DigitalSignatures](../../digitalsignatureutil/)
* assembly [Aspose.Words](../../../)
