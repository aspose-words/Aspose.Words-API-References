---
title: RtfSaveOptions.ExportImagesForOldReaders
second_title: Aspose.Words für .NET-API-Referenz
description: RtfSaveOptions eigendom. Gibt an ob die Schlüsselwörter für alte Reader in RTF geschrieben werden oder nicht. Dies kann die Größe des RTFDokuments erheblich beeinflussen. Standardwert istStimmt .
type: docs
weight: 30
url: /de/net/aspose.words.saving/rtfsaveoptions/exportimagesforoldreaders/
---
## RtfSaveOptions.ExportImagesForOldReaders property

Gibt an, ob die Schlüsselwörter für "alte Reader" in RTF geschrieben werden oder nicht. Dies kann die Größe des RTF-Dokuments erheblich beeinflussen. Standardwert ist`Stimmt` .

```csharp
public bool ExportImagesForOldReaders { get; set; }
```

### Bemerkungen

"Alte Lesegeräte" sind Anwendungen vor Microsoft Word 97 und auch WordPad. Wenn diese Option aktiviert ist`Stimmt` Aspose.Words schreibt zusätzliche RTF-Schlüsselwörter. Diese Schlüsselwörter ermöglichen die korrekte Anzeige des Dokuments, wenn es in einer "alten Reader"-Anwendung geöffnet wird, können aber die Größe des Dokuments erheblich erhöhen.

Wenn Sie diese Option auf setzen`FALSCH`, dann werden in "alten Readern" nur Bilder in den Formaten WMF, EMF und BMP angezeigt.

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

* class [RtfSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../rtfsaveoptions/)
* Montage [Aspose.Words](../../../)


