---
title: FileFormatUtil.DetectFileFormat
linktitle: DetectFileFormat
articleTitle: DetectFileFormat
second_title: Aspose.Words für .NET
description: Identifizieren Sie Dokumentformate schnell mit der DetectFileFormat-Methode von FileFormatUtil. Erhalten Sie genaue Formatinformationen für eine effiziente Dateiverwaltung.
type: docs
weight: 30
url: /de/net/aspose.words/fileformatutil/detectfileformat/
---
## DetectFileFormat(*string*) {#detectfileformat_1}

Erkennt und gibt die Informationen zum Format eines in einer Datei gespeicherten Dokuments zurück.

```csharp
public static FileFormatInfo DetectFileFormat(string fileName)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fileName | String | Der Dateiname. |

### Rückgabewert

A[`FileFormatInfo`](../../fileformatinfo/) Objekt, das die erkannten Informationen enthält.

## Bemerkungen

Selbst wenn diese Methode das Dokumentformat erkennt, garantiert sie nicht , dass das angegebene Dokument gültig ist. Diese Methode erkennt das Dokumentformat nur, indem Daten gelesen werden, die für die Erkennung ausreichen. Um die Gültigkeit eines Dokuments vollständig zu überprüfen , müssen Sie das Dokument in ein[`Document`](../../document/) Objekt.

Diese Methode wirft[`FileCorruptedException`](../../filecorruptedexception/) wenn das Format erkannt wird, die Erkennung jedoch aufgrund einer Beschädigung nicht abgeschlossen werden kann.

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

* class [FileFormatInfo](../../fileformatinfo/)
* class [FileFormatUtil](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)

---

## DetectFileFormat(*Stream*) {#detectfileformat}

Erkennt und gibt die Informationen zum Format eines in einem Stream gespeicherten Dokuments zurück.

```csharp
public static FileFormatInfo DetectFileFormat(Stream stream)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| stream | Stream | Der Bach. |

### Rückgabewert

A[`FileFormatInfo`](../../fileformatinfo/) Objekt, das die erkannten Informationen enthält.

## Bemerkungen

Der Stream muss am Anfang des Dokuments positioniert werden.

Wenn diese Methode zurückkehrt, wird die Position im Stream auf die ursprüngliche Position zurückgesetzt.

Selbst wenn diese Methode das Dokumentformat erkennt, garantiert sie nicht , dass das angegebene Dokument gültig ist. Diese Methode erkennt das Dokumentformat nur, indem Daten gelesen werden, die für die Erkennung ausreichen. Um die Gültigkeit eines Dokuments vollständig zu überprüfen , müssen Sie das Dokument in ein[`Document`](../../document/) Objekt.

Diese Methode wirft[`FileCorruptedException`](../../filecorruptedexception/) wenn das Format erkannt wird, die Erkennung jedoch aufgrund einer Beschädigung nicht abgeschlossen werden kann.

## Beispiele

Zeigt, wie die FileFormatUtil-Methoden zum Erkennen des Formats eines Dokuments verwendet werden.

```csharp
// Laden Sie ein Dokument aus einer Datei, der eine Dateierweiterung fehlt, und ermitteln Sie dann das Dateiformat.
using (FileStream docStream = File.OpenRead(MyDir + "Word document with missing file extension"))
{
    FileFormatInfo info = FileFormatUtil.DetectFileFormat(docStream);
    LoadFormat loadFormat = info.LoadFormat;

    Assert.AreEqual(LoadFormat.Doc, loadFormat);

    // Unten sind zwei Methoden zum Konvertieren eines LoadFormats in das entsprechende SaveFormat.
    // 1 – Holen Sie sich die Dateierweiterungszeichenfolge für das LoadFormat und dann das entsprechende SaveFormat aus dieser Zeichenfolge:
    string fileExtension = FileFormatUtil.LoadFormatToExtension(loadFormat);
    SaveFormat saveFormat = FileFormatUtil.ExtensionToSaveFormat(fileExtension);

    // 2 - Konvertieren Sie das LoadFormat direkt in sein SaveFormat:
    saveFormat = FileFormatUtil.LoadFormatToSaveFormat(loadFormat);

    // Laden Sie ein Dokument aus dem Stream und speichern Sie es dann mit der automatisch erkannten Dateierweiterung.
    Document doc = new Document(docStream);

    Assert.AreEqual(".doc", FileFormatUtil.SaveFormatToExtension(saveFormat));

    doc.Save(ArtifactsDir + "File.SaveToDetectedFileFormat" + FileFormatUtil.SaveFormatToExtension(saveFormat));
}
```

### Siehe auch

* class [FileFormatInfo](../../fileformatinfo/)
* class [FileFormatUtil](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
