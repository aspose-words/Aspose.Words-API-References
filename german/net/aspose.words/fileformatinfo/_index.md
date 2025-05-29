---
title: FileFormatInfo Class
linktitle: FileFormatInfo
articleTitle: FileFormatInfo
second_title: Aspose.Words für .NET
description: Entdecken Sie die Aspose.Words.FileFormatInfo-Klasse zur effizienten Erkennung von Dokumentformaten. Greifen Sie auf detaillierte Daten zu, um Ihre Dateiverwaltungslösungen zu verbessern.
type: docs
weight: 3220
url: /de/net/aspose.words/fileformatinfo/
---
## FileFormatInfo class

Enthält Daten, die zurückgegeben wurden von[`FileFormatUtil`](../fileformatutil/) Methoden zur Erkennung von Dokumentformaten.

Um mehr zu erfahren, besuchen Sie die[Dateiformat erkennen und Formatkompatibilität prüfen](https://docs.aspose.com/words/net/detect-file-format-and-check-format-compatibility/) Dokumentationsartikel.

```csharp
public class FileFormatInfo
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Encoding](../../aspose.words/fileformatinfo/encoding/) { get; } | Ruft die erkannte Kodierung ab, sofern sie auf das aktuelle Dokumentformat anwendbar ist. Derzeit wird die Kodierung nur für HTML-Dokumente erkannt. |
| [HasDigitalSignature](../../aspose.words/fileformatinfo/hasdigitalsignature/) { get; } | Rückgaben`WAHR`wenn dieses Dokument eine digitale Signatur enthält. Diese Eigenschaft informiert lediglich darüber, dass ein Dokument eine digitale Signatur enthält, gibt aber nicht an, ob die Signatur gültig ist oder nicht. |
| [HasMacros](../../aspose.words/fileformatinfo/hasmacros/) { get; } | Rückgaben`WAHR` wenn dieses Dokument VBA-Makros enthält. |
| [IsEncrypted](../../aspose.words/fileformatinfo/isencrypted/) { get; } | Rückgaben`WAHR` wenn das Dokument verschlüsselt ist und zum Öffnen ein Kennwort erforderlich ist. |
| [LoadFormat](../../aspose.words/fileformatinfo/loadformat/) { get; } | Ruft das erkannte Dokumentformat ab. |

## Bemerkungen

Sie erstellen keine Instanzen dieser Klasse direkt. Objekte dieser Klasse werden zurückgegeben von [`DetectFileFormat`](../fileformatutil/detectfileformat/) Methoden.

## Beispiele

Zeigt, wie die FileFormatUtil-Klasse zum Erkennen des Dokumentformats und der Verschlüsselung verwendet wird.

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

* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)
