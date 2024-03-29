---
title: RtfSaveOptions.SaveFormat
linktitle: SaveFormat
articleTitle: SaveFormat
second_title: Aspose.Words für .NET
description: RtfSaveOptions SaveFormat eigendom. Gibt das Format an in dem das Dokument gespeichert wird wenn dieses Speicheroptionsobjekt verwendet wird. Kann nur seinRtf  in C#.
type: docs
weight: 40
url: /de/net/aspose.words.saving/rtfsaveoptions/saveformat/
---
## RtfSaveOptions.SaveFormat property

Gibt das Format an, in dem das Dokument gespeichert wird, wenn dieses Speicheroptionsobjekt verwendet wird. Kann nur seinRtf .

```csharp
public override SaveFormat SaveFormat { get; set; }
```

## Beispiele

Zeigt, wie ein Dokument mit benutzerdefinierten Optionen im RTF-Format gespeichert wird.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Erstellen Sie ein „RtfSaveOptions“-Objekt, um es an die „Save“-Methode des Dokuments zu übergeben, um zu ändern, wie wir es in einem RTF speichern.
RtfSaveOptions options = new RtfSaveOptions();

Assert.AreEqual(SaveFormat.Rtf, options.SaveFormat);

// Setzen Sie die Eigenschaft „ExportCompactSize“ auf „true“.
// Reduzieren Sie die Größe des gespeicherten Dokuments auf Kosten der Rechts-nach-Links-Textkompatibilität.
options.ExportCompactSize = true;

// Setzen Sie die Eigenschaft „ExportImagesFotOldReaders“ auf „true“, um zusätzliche Schlüsselwörter zu verwenden, um sicherzustellen, dass unser Dokument korrekt ist
// kompatibel mit Lesegeräten vor Microsoft Word 97 und WordPad.
// Setzen Sie die Eigenschaft „ExportImagesFotOldReaders“ auf „false“, um die Größe des Dokuments zu reduzieren.
// aber verhindern, dass alte Leser alle Nicht-Metadateien oder BMP-Bilder lesen können, die das Dokument möglicherweise enthält.
options.ExportImagesForOldReaders = exportImagesForOldReaders;

doc.Save(ArtifactsDir + "RtfSaveOptions.ExportImages.rtf", options);
```

### Siehe auch

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [RtfSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
