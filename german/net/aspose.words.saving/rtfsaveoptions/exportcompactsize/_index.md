---
title: RtfSaveOptions.ExportCompactSize
second_title: Aspose.Words für .NET-API-Referenz
description: RtfSaveOptions eigendom. Ermöglicht es ausgegebene RTFDokumente kleiner zu machen aber wenn sie RTLText von rechts nach links enthalten wird dieser nicht korrekt angezeigt. Der Standardwert istFALSCH .
type: docs
weight: 20
url: /de/net/aspose.words.saving/rtfsaveoptions/exportcompactsize/
---
## RtfSaveOptions.ExportCompactSize property

Ermöglicht es, ausgegebene RTF-Dokumente kleiner zu machen, aber wenn sie RTL-Text (von rechts nach links) enthalten, wird dieser nicht korrekt angezeigt. Der Standardwert ist`FALSCH` .

```csharp
public bool ExportCompactSize { get; set; }
```

### Bemerkungen

Wenn das Dokument, das Sie mit Aspose.Words in RTF konvertieren möchten, in Sprachen wie Arabisch keinen von rechts nach links verlaufenden Text enthält , können Sie diese Option auf einstellen`Stimmt` , um die Größe des resultierenden RTF zu reduzieren.

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


