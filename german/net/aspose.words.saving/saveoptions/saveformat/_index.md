---
title: SaveOptions.SaveFormat
linktitle: SaveFormat
articleTitle: SaveFormat
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie Sie mit der SaveOptions SaveFormat-Eigenschaft mühelos das Speicherformat Ihres Dokuments auswählen und so optimale Flexibilität und Kontrolle erreichen.
type: docs
weight: 130
url: /de/net/aspose.words.saving/saveoptions/saveformat/
---
## SaveOptions.SaveFormat property

Gibt das Format an, in dem das Dokument gespeichert wird, wenn dieses Speicheroptionsobjekt verwendet wird.

```csharp
public abstract SaveFormat SaveFormat { get; set; }
```

## Beispiele

Zeigt, wie beim Speichern eines Dokuments im EPUB-Format eine bestimmte Kodierung verwendet wird.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Verwenden Sie ein SaveOptions-Objekt, um die Kodierung für ein Dokument anzugeben, das wir speichern möchten.
HtmlSaveOptions saveOptions = new HtmlSaveOptions();
saveOptions.SaveFormat = SaveFormat.Epub;
saveOptions.Encoding = Encoding.UTF8;

// Standardmäßig enthält ein Ausgabedokument im EPUB-Format seinen gesamten Inhalt in einem HTML-Teil.
// Ein Split-Kriterium ermöglicht es uns, das Dokument in mehrere HTML-Teile zu segmentieren.
// Wir legen die Kriterien fest, um das Dokument in Überschriftenabsätze aufzuteilen.
// Dies ist nützlich für Leser, die keine HTML-Dateien lesen können, die eine bestimmte Größe überschreiten.
saveOptions.DocumentSplitCriteria = DocumentSplitCriteria.HeadingParagraph;

// Geben Sie an, dass wir Dokumenteigenschaften exportieren möchten.
saveOptions.ExportDocumentProperties = true;

doc.Save(ArtifactsDir + "HtmlSaveOptions.Doc2EpubSaveOptions.epub", saveOptions);
```

### Siehe auch

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [SaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
