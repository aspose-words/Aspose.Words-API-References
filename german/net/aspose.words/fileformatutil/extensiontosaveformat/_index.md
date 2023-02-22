---
title: FileFormatUtil.ExtensionToSaveFormat
second_title: Aspose.Words für .NET-API-Referenz
description: FileFormatUtil methode. Konvertiert eine Dateinamenerweiterung in aSaveFormat wert.
type: docs
weight: 40
url: /de/net/aspose.words/fileformatutil/extensiontosaveformat/
---
## FileFormatUtil.ExtensionToSaveFormat method

Konvertiert eine Dateinamenerweiterung in a[`SaveFormat`](../../saveformat/) wert.

```csharp
public static SaveFormat ExtensionToSaveFormat(string extension)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| extension | String | Die Dateierweiterung. Kann mit oder ohne führenden Punkt sein. Groß- und Kleinschreibung beachten. |

### Ausnahmen

| Ausnahme | Bedingung |
| --- | --- |
| ArgumentNullException | Wird ausgelöst, wenn der Parameter null ist. |

### Bemerkungen

Wenn die Erweiterung nicht erkannt werden kann, wird zurückgegebenUnknown.

### Beispiele

Zeigt, wie die FileFormatUtil-Methoden verwendet werden, um das Format eines Dokuments zu erkennen.

```csharp
// Laden Sie ein Dokument aus einer Datei, der eine Dateierweiterung fehlt, und erkennen Sie dann das Dateiformat.
using (FileStream docStream = File.OpenRead(MyDir + "Word document with missing file extension"))
{
    FileFormatInfo info = FileFormatUtil.DetectFileFormat(docStream);
    LoadFormat loadFormat = info.LoadFormat;

    Assert.AreEqual(LoadFormat.Doc, loadFormat);

    // Unten sind zwei Methoden zum Konvertieren eines LoadFormats in sein entsprechendes SaveFormat.
    // 1 - Holen Sie sich die Dateierweiterungszeichenfolge für das LoadFormat, dann erhalten Sie das entsprechende SaveFormat aus dieser Zeichenfolge:
    string fileExtension = FileFormatUtil.LoadFormatToExtension(loadFormat);
    SaveFormat saveFormat = FileFormatUtil.ExtensionToSaveFormat(fileExtension);

    // 2 - Konvertiere das LoadFormat direkt in sein SaveFormat:
    saveFormat = FileFormatUtil.LoadFormatToSaveFormat(loadFormat);

    // Laden Sie ein Dokument aus dem Stream und speichern Sie es dann in der automatisch erkannten Dateierweiterung.
    Document doc = new Document(docStream);

    Assert.AreEqual(".doc", FileFormatUtil.SaveFormatToExtension(saveFormat));

    doc.Save(ArtifactsDir + "File.SaveToDetectedFileFormat" + FileFormatUtil.SaveFormatToExtension(saveFormat));
}
```

### Siehe auch

* enum [SaveFormat](../../saveformat/)
* class [FileFormatUtil](../)
* namensraum [Aspose.Words](../../fileformatutil/)
* Montage [Aspose.Words](../../../)


