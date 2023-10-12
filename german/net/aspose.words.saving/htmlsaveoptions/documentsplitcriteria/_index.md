---
title: HtmlSaveOptions.DocumentSplitCriteria
second_title: Aspose.Words für .NET-API-Referenz
description: HtmlSaveOptions eigendom. Gibt an wie das Dokument beim Speichern aufgeteilt werden sollHtml  Epub oderAzw3 Format. Standard istNone für HTML und HeadingParagraph für EPUB und AZW3.
type: docs
weight: 80
url: /de/net/aspose.words.saving/htmlsaveoptions/documentsplitcriteria/
---
## HtmlSaveOptions.DocumentSplitCriteria property

Gibt an, wie das Dokument beim Speichern aufgeteilt werden sollHtml , Epub oderAzw3 Format. Standard istNone für HTML und HeadingParagraph für EPUB und AZW3.

```csharp
public DocumentSplitCriteria DocumentSplitCriteria { get; set; }
```

### Bemerkungen

Normalerweise möchten Sie, dass ein Dokument als einzelne Datei im HTML-Format gespeichert wird. In manchen Fällen ist es jedoch vorzuziehen, die Ausgabe in mehrere kleinere HTML-Seiten aufzuteilen. Beim Speichern im HTML-Format werden diese Seiten in einzelne Dateien oder Streams ausgegeben. Beim Speichern im EPUB-Format werden sie in entsprechende Pakete eingebunden.

Beim Speichern im MHTML-Format kann ein Dokument nicht geteilt werden.

### Beispiele

Zeigt, wie beim Speichern eines Dokuments im .epub-Format eine bestimmte Kodierung verwendet wird.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Verwenden Sie ein SaveOptions-Objekt, um die Codierung für ein Dokument anzugeben, das wir speichern möchten.
HtmlSaveOptions saveOptions = new HtmlSaveOptions();
saveOptions.SaveFormat = SaveFormat.Epub;
saveOptions.Encoding = Encoding.UTF8;

// Standardmäßig enthält ein .epub-Ausgabedokument seinen gesamten Inhalt in einem HTML-Teil.
// Ein Split-Kriterium ermöglicht es uns, das Dokument in mehrere HTML-Teile zu segmentieren.
// Wir legen die Kriterien fest, um das Dokument in Überschriftenabsätze aufzuteilen.
// Dies ist nützlich für Leser, die keine HTML-Dateien lesen können, die größer als eine bestimmte Größe sind.
saveOptions.DocumentSplitCriteria = DocumentSplitCriteria.HeadingParagraph;

// Geben Sie an, dass wir Dokumenteigenschaften exportieren möchten.
saveOptions.ExportDocumentProperties = true;

doc.Save(ArtifactsDir + "HtmlSaveOptions.Doc2EpubSaveOptions.epub", saveOptions);
```

### Siehe auch

* enum [DocumentSplitCriteria](../../documentsplitcriteria/)
* class [HtmlSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../htmlsaveoptions/)
* Montage [Aspose.Words](../../../)


