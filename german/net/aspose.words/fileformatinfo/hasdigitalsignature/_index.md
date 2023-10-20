---
title: FileFormatInfo.HasDigitalSignature
linktitle: HasDigitalSignature
articleTitle: HasDigitalSignature
second_title: Aspose.Words für .NET
description: FileFormatInfo HasDigitalSignature eigendom. Gibt zurückWAHRwenn dieses Dokument eine digitale Signatur enthält. Diese Eigenschaft informiert lediglich darüber dass eine digitale Signatur in einem Dokument vorhanden ist  gibt jedoch nicht an ob die Signatur gültig ist oder nicht in C#.
type: docs
weight: 20
url: /de/net/aspose.words/fileformatinfo/hasdigitalsignature/
---
## FileFormatInfo.HasDigitalSignature property

Gibt zurück`WAHR`wenn dieses Dokument eine digitale Signatur enthält. Diese Eigenschaft informiert lediglich darüber, dass eine digitale Signatur in einem Dokument vorhanden ist, , gibt jedoch nicht an, ob die Signatur gültig ist oder nicht.

```csharp
public bool HasDigitalSignature { get; }
```

## Bemerkungen

Diese Eigenschaft hilft Ihnen beim Sortieren von Dokumenten, die digital signiert sind, von solchen, die nicht digital signiert sind. Wenn Sie Aspose.Words verwenden, um ein Dokument zu ändern und zu speichern, das digital signiert ist, geht die digitale Signatur verloren. Dies ist beabsichtigt, da eine digitale Signatur existiert, um die Authentizität eines Dokuments zu schützen. Mit dieser Eigenschaft können Sie digital signierte Dokumente erkennen, bevor Sie sie auf die gleiche Weise wie normale -Dokumente verarbeiten, und Maßnahmen ergreifen, um den Verlust der digitalen Signatur zu vermeiden, z. B. den Benutzer benachrichtigen.

## Beispiele

Zeigt, wie die FileFormatUtil-Klasse verwendet wird, um das Dokumentformat und das Vorhandensein digitaler Signaturen zu erkennen.

```csharp
// Verwenden Sie eine FileFormatInfo-Instanz, um zu überprüfen, ob ein Dokument nicht digital signiert ist.
FileFormatInfo info = FileFormatUtil.DetectFileFormat(MyDir + "Document.docx");

Assert.AreEqual(".docx", FileFormatUtil.LoadFormatToExtension(info.LoadFormat));
Assert.False(info.HasDigitalSignature);

CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);
DigitalSignatureUtil.Sign(MyDir + "Document.docx", ArtifactsDir + "File.DetectDigitalSignatures.docx",
    certificateHolder, new SignOptions() { SignTime = DateTime.Now });

// Verwenden Sie eine neue FileFormatInstance, um zu bestätigen, dass sie signiert ist.
info = FileFormatUtil.DetectFileFormat(ArtifactsDir + "File.DetectDigitalSignatures.docx");

Assert.True(info.HasDigitalSignature);

// Wir können die Signaturen eines signierten Dokuments in einer solchen Sammlung laden und darauf zugreifen.
Assert.AreEqual(1, DigitalSignatureUtil.LoadSignatures(ArtifactsDir + "File.DetectDigitalSignatures.docx").Count);
```

### Siehe auch

* class [FileFormatInfo](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
