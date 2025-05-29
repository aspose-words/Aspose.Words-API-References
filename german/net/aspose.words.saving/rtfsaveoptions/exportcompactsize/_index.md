---
title: RtfSaveOptions.ExportCompactSize
linktitle: ExportCompactSize
articleTitle: ExportCompactSize
second_title: Aspose.Words für .NET
description: Optimieren Sie die Größe von RTF-Dokumenten mit der Eigenschaft „ExportCompactSize“. Sorgen Sie für effiziente Speicherung bei gleichzeitiger Wahrung der Textintegrität, auch bei RTL-Inhalten.
type: docs
weight: 20
url: /de/net/aspose.words.saving/rtfsaveoptions/exportcompactsize/
---
## RtfSaveOptions.ExportCompactSize property

Ermöglicht die Verkleinerung von RTF-Ausgabedokumenten. Wenn diese jedoch RTL-Text (von rechts nach links) enthalten, wird dieser nicht korrekt angezeigt. Der Standardwert ist`FALSCH` .

```csharp
public bool ExportCompactSize { get; set; }
```

## Bemerkungen

Wenn das Dokument, das Sie mit Aspose.Words in RTF konvertieren möchten, keinen von rechts nach links geschriebenen Text in Sprachen wie Arabisch enthält, können Sie diese Option auf`WAHR` , um die Größe des resultierenden RTF zu reduzieren.

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
