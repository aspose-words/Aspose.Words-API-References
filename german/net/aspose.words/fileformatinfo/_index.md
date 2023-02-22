---
title: Class FileFormatInfo
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.FileFormatInfo klas. Enthält Daten die von zurückgegeben wurdenFileFormatUtil Methoden zur Erkennung des Dokumentformats.
type: docs
weight: 2630
url: /de/net/aspose.words/fileformatinfo/
---
## FileFormatInfo class

Enthält Daten, die von zurückgegeben wurden[`FileFormatUtil`](../fileformatutil/) Methoden zur Erkennung des Dokumentformats.

```csharp
public class FileFormatInfo
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Encoding](../../aspose.words/fileformatinfo/encoding/) { get; } | Ruft die erkannte Codierung ab, falls für das aktuelle Dokumentformat zutreffend. Erkennt derzeit nur die Codierung für HTML-Dokumente. |
| [HasDigitalSignature](../../aspose.words/fileformatinfo/hasdigitalsignature/) { get; } | Gibt wahr zurück, wenn dieses Dokument eine digitale Signatur enthält. Diese Eigenschaft informiert lediglich darüber, dass eine digitale Signatur auf einem Dokument vorhanden ist, gibt aber nicht an, ob die Signatur gültig ist oder nicht. |
| [IsEncrypted](../../aspose.words/fileformatinfo/isencrypted/) { get; } | Gibt „true“ zurück, wenn das Dokument verschlüsselt ist und zum Öffnen ein Passwort erfordert. |
| [LoadFormat](../../aspose.words/fileformatinfo/loadformat/) { get; } | Ruft das erkannte Dokumentformat ab. |

### Bemerkungen

Sie erstellen keine Instanzen dieser Klasse direkt. Objekte dieser Klasse werden von zurückgegeben[`DetectFileFormat`](../fileformatutil/detectfileformat/)Methoden.

### Beispiele

Zeigt, wie die FileFormatUtil-Klasse verwendet wird, um das Dokumentformat und die Verschlüsselung zu erkennen.

```csharp
Document doc = new Document();

// Konfigurieren Sie ein SaveOptions-Objekt, um das Dokument zu verschlüsseln
// mit einem Passwort, wenn wir es speichern, und speichern Sie dann das Dokument.
OdtSaveOptions saveOptions = new OdtSaveOptions(SaveFormat.Odt);
saveOptions.Password = "MyPassword";

doc.Save(ArtifactsDir + "File.DetectDocumentEncryption.odt", saveOptions);

// Überprüfen Sie den Dateityp unseres Dokuments und seinen Verschlüsselungsstatus.
FileFormatInfo info = FileFormatUtil.DetectFileFormat(ArtifactsDir + "File.DetectDocumentEncryption.odt");

Assert.AreEqual(".odt", FileFormatUtil.LoadFormatToExtension(info.LoadFormat));
Assert.True(info.IsEncrypted);
```

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

// Wir können die Signaturen eines signierten Dokuments in einer Sammlung wie dieser laden und darauf zugreifen.
Assert.AreEqual(1, DigitalSignatureUtil.LoadSignatures(ArtifactsDir + "File.DetectDigitalSignatures.docx").Count);
```

### Siehe auch

* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)


