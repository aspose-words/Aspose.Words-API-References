---
title: PdfSaveOptions.ExportLanguageToSpanTag
second_title: Aspose.Words für .NET-API-Referenz
description: PdfSaveOptions eigendom. Ruft einen Wert ab oder legt diesen fest der bestimmt ob ein SpanTag in der Dokumentstruktur erstellt werden soll um die Textsprache zu exportieren.
type: docs
weight: 150
url: /de/net/aspose.words.saving/pdfsaveoptions/exportlanguagetospantag/
---
## PdfSaveOptions.ExportLanguageToSpanTag property

Ruft einen Wert ab oder legt diesen fest, der bestimmt, ob ein „Span“-Tag in der Dokumentstruktur erstellt werden soll, um die Textsprache zu exportieren.

```csharp
public bool ExportLanguageToSpanTag { get; set; }
```

### Bemerkungen

Der Standardwert ist`FALSCH`und das Attribut „Lang“ wird an eine markierte Inhaltssequenz in einem Seiteninhaltsstrom angehängt.

Wenn der Wert ist`WAHR` Das Tag „Span“ wird für den Text mit der nicht standardmäßigen Sprache erstellt und das Attribut „Lang“ wird an dieses Tag angehängt.

Dieser Wert wird ignoriert, wenn[`ExportDocumentStructure`](../exportdocumentstructure/) Ist`FALSCH` .

### Beispiele

Zeigt, wie ein „Span“-Tag in der Dokumentstruktur erstellt wird, um die Textsprache zu exportieren.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");
builder.Writeln("Hola mundo!");

PdfSaveOptions saveOptions = new PdfSaveOptions
{
    // Hinweis: Wenn „ExportDocumentStructure“ false ist, wird „ExportLanguageToSpanTag“ ignoriert.
    ExportDocumentStructure = true, ExportLanguageToSpanTag = true
};

doc.Save(ArtifactsDir + "PdfSaveOptions.ExportLanguageToSpanTag.pdf", saveOptions);
```

### Siehe auch

* class [PdfSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../pdfsaveoptions/)
* Montage [Aspose.Words](../../../)


