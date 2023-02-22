---
title: Document.OriginalFileName
second_title: Aspose.Words für .NET-API-Referenz
description: Document eigendom. Ruft den ursprünglichen Dateinamen des Dokuments ab.
type: docs
weight: 270
url: /de/net/aspose.words/document/originalfilename/
---
## Document.OriginalFileName property

Ruft den ursprünglichen Dateinamen des Dokuments ab.

```csharp
public string OriginalFileName { get; }
```

### Bemerkungen

Gibt null zurück, wenn das Dokument aus einem Stream geladen oder leer erstellt wurde.

### Beispiele

Zeigt, wie Details zum Ladevorgang eines Dokuments abgerufen werden.

```csharp
Document doc = new Document(MyDir + "Document.docx");

Assert.AreEqual(MyDir + "Document.docx", doc.OriginalFileName);
Assert.AreEqual(LoadFormat.Docx, doc.OriginalLoadFormat);
```

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

* class [Document](../)
* namensraum [Aspose.Words](../../document/)
* Montage [Aspose.Words](../../../)


