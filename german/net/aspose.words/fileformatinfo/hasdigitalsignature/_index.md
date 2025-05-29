---
title: FileFormatInfo.HasDigitalSignature
linktitle: HasDigitalSignature
articleTitle: HasDigitalSignature
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „FileFormatInfo HasDigitalSignature“ – überprüfen Sie schnell, ob Ihr Dokument eine digitale Signatur enthält, und erhöhen Sie so die Sicherheit und Authentizität.
type: docs
weight: 20
url: /de/net/aspose.words/fileformatinfo/hasdigitalsignature/
---
## FileFormatInfo.HasDigitalSignature property

Rückgaben`WAHR`wenn dieses Dokument eine digitale Signatur enthält. Diese Eigenschaft informiert lediglich darüber, dass ein Dokument eine digitale Signatur enthält, gibt aber nicht an, ob die Signatur gültig ist oder nicht.

```csharp
public bool HasDigitalSignature { get; }
```

## Bemerkungen

Diese Eigenschaft hilft Ihnen, digital signierte Dokumente von nicht signierten zu trennen. Wenn Sie Aspose.Words verwenden, um ein digital signiertes Dokument zu ändern und zu speichern, geht die digitale Signatur verloren. Dies ist beabsichtigt, da eine digitale Signatur die Authentizität eines Dokuments schützt. Mit dieser Eigenschaft können Sie digital signierte Dokumente vor der Verarbeitung wie normale Dokumente erkennen und Maßnahmen ergreifen, um den Verlust der digitalen Signatur zu vermeiden, z. B. den Benutzer benachrichtigen.

## Beispiele

Zeigt, wie die FileFormatUtil-Klasse verwendet wird, um das Dokumentformat und das Vorhandensein digitaler Signaturen zu erkennen.

```csharp
// Verwenden Sie eine FileFormatInfo-Instanz, um zu überprüfen, ob ein Dokument digital signiert ist.
FileFormatInfo info = FileFormatUtil.DetectFileFormat(MyDir + "Document.docx");

Assert.AreEqual(".docx", FileFormatUtil.LoadFormatToExtension(info.LoadFormat));
Assert.False(info.HasDigitalSignature);

CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);
SignOptions signOptions = new SignOptions() { SignTime = DateTime.Now };
DigitalSignatureUtil.Sign(MyDir + "Document.docx", ArtifactsDir + "File.DetectDigitalSignatures.docx",
    certificateHolder, signOptions);

// Verwenden Sie eine neue FileFormatInstance, um zu bestätigen, dass sie signiert ist.
info = FileFormatUtil.DetectFileFormat(ArtifactsDir + "File.DetectDigitalSignatures.docx");

Assert.True(info.HasDigitalSignature);

// Wir können die Signaturen eines signierten Dokuments in einer Sammlung wie dieser laden und darauf zugreifen.
Assert.AreEqual(1, DigitalSignatureUtil.LoadSignatures(ArtifactsDir + "File.DetectDigitalSignatures.docx").Count);
```

### Siehe auch

* class [FileFormatInfo](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
