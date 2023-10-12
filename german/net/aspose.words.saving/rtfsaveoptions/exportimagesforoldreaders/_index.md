---
title: RtfSaveOptions.ExportImagesForOldReaders
second_title: Aspose.Words für .NET-API-Referenz
description: RtfSaveOptions eigendom. Gibt an ob die Schlüsselwörter für alte Leser in RTF geschrieben werden oder nicht. Dies kann die Größe des RTFDokuments erheblich beeinflussen. Der Standardwert istWAHR .
type: docs
weight: 30
url: /de/net/aspose.words.saving/rtfsaveoptions/exportimagesforoldreaders/
---
## RtfSaveOptions.ExportImagesForOldReaders property

Gibt an, ob die Schlüsselwörter für „alte Leser“ in RTF geschrieben werden oder nicht. Dies kann die Größe des RTF-Dokuments erheblich beeinflussen. Der Standardwert ist`WAHR` .

```csharp
public bool ExportImagesForOldReaders { get; set; }
```

### Bemerkungen

„Alte Leser“ sind Anwendungen vor Microsoft Word 97 und auch WordPad. Wenn diese Option aktiviert ist`WAHR` Aspose.Words schreibt zusätzliche RTF-Schlüsselwörter. Diese Schlüsselwörter ermöglichen die korrekte Anzeige des Dokuments beim Öffnen in einer „alten Reader“-Anwendung, können jedoch die Größe des Dokuments erheblich erhöhen.

Wenn Sie diese Option auf setzen`FALSCH`, dann werden in „alten Readern“ nur Bilder in den Formaten WMF, EMF und BMP angezeigt.

### Beispiele

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

* class [RtfSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../rtfsaveoptions/)
* Montage [Aspose.Words](../../../)


