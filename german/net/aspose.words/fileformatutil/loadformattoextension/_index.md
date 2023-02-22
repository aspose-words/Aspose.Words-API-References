---
title: FileFormatUtil.LoadFormatToExtension
second_title: Aspose.Words für .NET-API-Referenz
description: FileFormatUtil methode. Wandelt einen Aufzählungswert im Ladeformat in eine Dateierweiterung um. Die zurückgegebene Erweiterung ist eine Zeichenfolge in Kleinbuchstaben mit einem führenden Punkt.
type: docs
weight: 60
url: /de/net/aspose.words/fileformatutil/loadformattoextension/
---
## FileFormatUtil.LoadFormatToExtension method

Wandelt einen Aufzählungswert im Ladeformat in eine Dateierweiterung um. Die zurückgegebene Erweiterung ist eine Zeichenfolge in Kleinbuchstaben mit einem führenden Punkt.

```csharp
public static string LoadFormatToExtension(LoadFormat loadFormat)
```

### Ausnahmen

| Ausnahme | Bedingung |
| --- | --- |
| ArgumentException | Wirft, wenn nicht konvertiert werden kann. |

### Bemerkungen

DasWordML Wert wird in ".wml" konvertiert.

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

* enum [LoadFormat](../../loadformat/)
* class [FileFormatUtil](../)
* namensraum [Aspose.Words](../../fileformatutil/)
* Montage [Aspose.Words](../../../)


