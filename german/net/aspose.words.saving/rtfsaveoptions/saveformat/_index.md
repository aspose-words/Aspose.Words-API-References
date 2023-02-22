---
title: RtfSaveOptions.SaveFormat
second_title: Aspose.Words für .NET-API-Referenz
description: RtfSaveOptions eigendom. Gibt das Format an in dem das Dokument gespeichert wird wenn dieses Speicheroptionsobjekt verwendet wird. Kann nur seinRtf .
type: docs
weight: 40
url: /de/net/aspose.words.saving/rtfsaveoptions/saveformat/
---
## RtfSaveOptions.SaveFormat property

Gibt das Format an, in dem das Dokument gespeichert wird, wenn dieses Speicheroptionsobjekt verwendet wird. Kann nur seinRtf .

```csharp
public override SaveFormat SaveFormat { get; set; }
```

### Beispiele

Zeigt, wie ein Dokument mit benutzerdefinierten Optionen im RTF-Format gespeichert wird.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Erstellen Sie ein "RtfSaveOptions"-Objekt, das an die "Save"-Methode des Dokuments übergeben wird, um zu ändern, wie wir es in einem RTF speichern.
RtfSaveOptions options = new RtfSaveOptions();

Assert.AreEqual(SaveFormat.Rtf, options.SaveFormat);

// Setzen Sie die Eigenschaft "ExportCompactSize" auf "true".
// Reduzieren Sie die Größe des gespeicherten Dokuments auf Kosten der Textkompatibilität von rechts nach links.
options.ExportCompactSize = true;

// Setzen Sie die Eigenschaft "ExportImagesFotOldReaders" auf "true", um zusätzliche Schlüsselwörter zu verwenden, um sicherzustellen, dass unser Dokument ist
// kompatibel mit Pre-Microsoft Word 97 Readern und WordPad.
// Setzen Sie die Eigenschaft "ExportImagesFotOldReaders" auf "false", um die Größe des Dokuments zu reduzieren,
// aber verhindern, dass alte Reader alle Nicht-Metafile- oder BMP-Bilder lesen können, die das Dokument enthalten kann.
options.ExportImagesForOldReaders = exportImagesForOldReaders;

doc.Save(ArtifactsDir + "RtfSaveOptions.ExportImages.rtf", options);
```

### Siehe auch

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [RtfSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../rtfsaveoptions/)
* Montage [Aspose.Words](../../../)


