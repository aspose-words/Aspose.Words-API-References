---
title: RtfSaveOptions.SaveFormat
linktitle: SaveFormat
articleTitle: SaveFormat
second_title: Aspose.Words für .NET
description: Entdecken Sie die SaveFormat-Eigenschaft von RtfSaveOptions, um Ihre Dokumente mühelos im RTF-Format zu speichern und so Kompatibilität und einfaches Teilen sicherzustellen.
type: docs
weight: 40
url: /de/net/aspose.words.saving/rtfsaveoptions/saveformat/
---
## RtfSaveOptions.SaveFormat property

Gibt das Format an, in dem das Dokument gespeichert wird, wenn dieses Speicheroptionsobjekt verwendet wird. Kann nurRtf .

```csharp
public override SaveFormat SaveFormat { get; set; }
```

## Beispiele

Zeigt, wie ein Dokument mit benutzerdefinierten Optionen im RTF-Format gespeichert wird.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Erstellen Sie ein „RtfSaveOptions“-Objekt, das an die „Speichern“-Methode des Dokuments übergeben wird, um die Art und Weise zu ändern, wie wir es als RTF speichern.
RtfSaveOptions options = new RtfSaveOptions();

Assert.AreEqual(SaveFormat.Rtf, options.SaveFormat);

// Setzen Sie die Eigenschaft "ExportCompactSize" auf "true", um
// Reduzieren Sie die Größe des gespeicherten Dokuments auf Kosten der Rechts-nach-Links-Textkompatibilität.
options.ExportCompactSize = true;

// Setzen Sie die Eigenschaft "ExportImagesFotOldReaders" auf "true", um zusätzliche Schlüsselwörter zu verwenden, die sicherstellen, dass unser Dokument
// kompatibel mit Readern vor Microsoft Word 97 und WordPad.
// Setzen Sie die Eigenschaft „ExportImagesFotOldReaders“ auf „false“, um die Größe des Dokuments zu reduzieren.
// aber verhindern Sie, dass alte Reader alle Nicht-Metadateien oder BMP-Bilder lesen können, die das Dokument enthalten kann.
options.ExportImagesForOldReaders = exportImagesForOldReaders;

doc.Save(ArtifactsDir + "RtfSaveOptions.ExportImages.rtf", options);
```

### Siehe auch

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [RtfSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
