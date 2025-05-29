---
title: FileFormatUtil.LoadFormatToExtension
linktitle: LoadFormatToExtension
articleTitle: LoadFormatToExtension
second_title: Aspose.Words für .NET
description: Mit der Methode LoadFormatToExtension von FileFormatUtil können Sie Ladeformatwerte mühelos in Dateierweiterungen umwandeln. So erhalten Sie mühelos präzise, kleingeschriebene Erweiterungen!
type: docs
weight: 60
url: /de/net/aspose.words/fileformatutil/loadformattoextension/
---
## FileFormatUtil.LoadFormatToExtension method

Konvertiert einen im Ladeformat aufgezählten Wert in eine Dateierweiterung. Die zurückgegebene Erweiterung ist eine Zeichenfolge in Kleinbuchstaben mit einem führenden Punkt.

```csharp
public static string LoadFormatToExtension(LoadFormat loadFormat)
```

### Ausnahmen

| Ausnahme | Bedingung |
| --- | --- |
| ArgumentException | Wirft, wenn keine Konvertierung möglich ist. |

## Bemerkungen

DerWordML Der Wert wird in „.wml“ konvertiert.

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

* enum [LoadFormat](../../loadformat/)
* class [FileFormatUtil](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
