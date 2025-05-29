---
title: HtmlSaveOptions.ExportDocumentProperties
linktitle: ExportDocumentProperties
articleTitle: ExportDocumentProperties
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie ExportDocumentProperties von HtmlSaveOptions Ihre HTML-, MHTML- oder EPUB-Exporte durch die Einbeziehung wichtiger integrierter und benutzerdefinierter Dokumenteigenschaften verbessert.
type: docs
weight: 120
url: /de/net/aspose.words.saving/htmlsaveoptions/exportdocumentproperties/
---
## HtmlSaveOptions.ExportDocumentProperties property

Gibt an, ob integrierte und benutzerdefinierte Dokumenteigenschaften in HTML, MHTML oder EPUB exportiert werden sollen. Der Standardwert ist`FALSCH` .

```csharp
public bool ExportDocumentProperties { get; set; }
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

* class [HtmlSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
