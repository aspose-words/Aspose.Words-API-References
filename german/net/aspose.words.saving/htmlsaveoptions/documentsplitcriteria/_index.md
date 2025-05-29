---
title: HtmlSaveOptions.DocumentSplitCriteria
linktitle: DocumentSplitCriteria
articleTitle: DocumentSplitCriteria
second_title: Aspose.Words für .NET
description: Entdecken Sie die DocumentSplitCriteria-Eigenschaft von HtmlSaveOptions, um das Speichern von Dokumenten in den Formaten HTML, EPUB und AZW3 zu optimieren. Verbessern Sie noch heute Ihre Formatierungskontrolle!
type: docs
weight: 80
url: /de/net/aspose.words.saving/htmlsaveoptions/documentsplitcriteria/
---
## HtmlSaveOptions.DocumentSplitCriteria property

Gibt an, wie das Dokument beim Speichern aufgeteilt werden soll.Html , Epub oderAzw3 format. Standard istNone für HTML und HeadingParagraph für EPUB und AZW3.

```csharp
public DocumentSplitCriteria DocumentSplitCriteria { get; set; }
```

## Bemerkungen

Normalerweise möchten Sie ein Dokument als einzelne Datei im HTML-Format speichern. In manchen Fällen ist es jedoch vorzuziehen, die Ausgabe in mehrere kleinere HTML-Seiten aufzuteilen. Beim Speichern im HTML-Format werden diese Seiten in einzelne Dateien oder Streams ausgegeben. Beim Speichern im EPUB-Format werden sie in entsprechende Pakete integriert.

Beim Speichern im MHTML-Format kann ein Dokument nicht aufgeteilt werden.

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

* enum [DocumentSplitCriteria](../../documentsplitcriteria/)
* class [HtmlSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
