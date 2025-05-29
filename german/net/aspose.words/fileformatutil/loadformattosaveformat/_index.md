---
title: FileFormatUtil.LoadFormatToSaveFormat
linktitle: LoadFormatToSaveFormat
articleTitle: LoadFormatToSaveFormat
second_title: Aspose.Words für .NET
description: Konvertieren Sie LoadFormat mühelos in SaveFormat mit der LoadFormatToSaveFormat-Methode von FileFormatUtil. Optimieren Sie noch heute Ihre Dateiverwaltung!
type: docs
weight: 70
url: /de/net/aspose.words/fileformatutil/loadformattosaveformat/
---
## FileFormatUtil.LoadFormatToSaveFormat method

Konvertiert eine[`LoadFormat`](../../loadformat/) Wert zu einem[`SaveFormat`](../../saveformat/) Wert wenn möglich.

```csharp
public static SaveFormat LoadFormatToSaveFormat(LoadFormat loadFormat)
```

### Ausnahmen

| Ausnahme | Bedingung |
| --- | --- |
| ArgumentException | Wirft, wenn keine Konvertierung möglich ist. |

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

* enum [SaveFormat](../../saveformat/)
* enum [LoadFormat](../../loadformat/)
* class [FileFormatUtil](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
