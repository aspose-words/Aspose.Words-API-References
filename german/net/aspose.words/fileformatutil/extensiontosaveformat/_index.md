---
title: FileFormatUtil.ExtensionToSaveFormat
linktitle: ExtensionToSaveFormat
articleTitle: ExtensionToSaveFormat
second_title: Aspose.Words für .NET
description: Mit der FileFormatUtil ExtensionToSaveFormat-Methode können Sie Dateinamenerweiterungen mühelos in SaveFormat-Werte konvertieren. Vereinfachen Sie noch heute Ihre Dateiverwaltung!
type: docs
weight: 40
url: /de/net/aspose.words/fileformatutil/extensiontosaveformat/
---
## FileFormatUtil.ExtensionToSaveFormat method

Wandelt eine Dateinamenerweiterung in eine[`SaveFormat`](../../saveformat/) Wert.

```csharp
public static SaveFormat ExtensionToSaveFormat(string extension)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| extension | String | Die Dateierweiterung. Kann mit oder ohne führenden Punkt angegeben werden. Groß-/Kleinschreibung wird nicht berücksichtigt. |

### Ausnahmen

| Ausnahme | Bedingung |
| --- | --- |
| ArgumentNullException | Wirft, wenn der Parameter`null`. |

## Bemerkungen

Wenn die Erweiterung nicht erkannt wird, gibtUnknown.

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
* class [FileFormatUtil](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
