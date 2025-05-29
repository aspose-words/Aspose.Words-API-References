---
title: RtfSaveOptions.ExportImagesForOldReaders
linktitle: ExportImagesForOldReaders
articleTitle: ExportImagesForOldReaders
second_title: Aspose.Words für .NET
description: Optimieren Sie Ihre RTF-Dokumente mit der Eigenschaft „ExportImagesForOldReaders“. Steuern Sie die Einbindung von Schlüsselwörtern für ältere Reader, was sich auf Dateigröße und Leistung auswirkt.
type: docs
weight: 30
url: /de/net/aspose.words.saving/rtfsaveoptions/exportimagesforoldreaders/
---
## RtfSaveOptions.ExportImagesForOldReaders property

Gibt an, ob die Schlüsselwörter für "alte Leser" in RTF geschrieben werden oder nicht. Dies kann die Größe des RTF-Dokuments erheblich beeinflussen. Der Standardwert ist`WAHR` .

```csharp
public bool ExportImagesForOldReaders { get; set; }
```

## Bemerkungen

"Alte Reader" sind Anwendungen vor Microsoft Word 97 und auch WordPad. Wenn diese Option`WAHR` Aspose.Words schreibt zusätzliche RTF-Schlüsselwörter. Diese Schlüsselwörter ermöglichen die korrekte Anzeige des Dokuments beim Öffnen in einer „alten Reader“-Anwendung, können aber die Größe des Dokuments erheblich erhöhen.

Wenn Sie diese Option auf`FALSCH`dann werden in „alten Readern“ nur Bilder im WMF-, EMF- und BMP-Format angezeigt.

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

* class [RtfSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
