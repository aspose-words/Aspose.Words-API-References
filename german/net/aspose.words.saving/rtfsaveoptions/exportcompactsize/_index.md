---
title: RtfSaveOptions.ExportCompactSize
linktitle: ExportCompactSize
articleTitle: ExportCompactSize
second_title: Aspose.Words für .NET
description: RtfSaveOptions ExportCompactSize eigendom. Ermöglicht die Verkleinerung ausgegebener RTFDokumente. Wenn sie jedoch RTLText von rechts nach links enthalten wird dieser nicht korrekt angezeigt. Der Standardwert istFALSCH  in C#.
type: docs
weight: 20
url: /de/net/aspose.words.saving/rtfsaveoptions/exportcompactsize/
---
## RtfSaveOptions.ExportCompactSize property

Ermöglicht die Verkleinerung ausgegebener RTF-Dokumente. Wenn sie jedoch RTL-Text (von rechts nach links) enthalten, wird dieser nicht korrekt angezeigt. Der Standardwert ist`FALSCH` .

```csharp
public bool ExportCompactSize { get; set; }
```

## Bemerkungen

Wenn das Dokument, das Sie mit Aspose.Words in RTF konvertieren möchten, keinen von rechts nach links verlaufenden Text in Sprachen wie Arabisch enthält, können Sie diese Option auf setzen`WAHR` , um die Größe des resultierenden RTF zu reduzieren.

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

* class [RtfSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
