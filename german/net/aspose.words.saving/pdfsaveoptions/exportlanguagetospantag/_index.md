---
title: PdfSaveOptions.ExportLanguageToSpanTag
linktitle: ExportLanguageToSpanTag
articleTitle: ExportLanguageToSpanTag
second_title: Aspose.Words für .NET
description: Entdecken Sie die ExportLanguageToSpanTag-Eigenschaft von PdfSaveOptions. Steuern Sie den Textsprachenexport mit Span-Tags für eine verbesserte Dokumentstruktur und Zugänglichkeit.
type: docs
weight: 150
url: /de/net/aspose.words.saving/pdfsaveoptions/exportlanguagetospantag/
---
## PdfSaveOptions.ExportLanguageToSpanTag property

Ruft einen Wert ab oder legt einen Wert fest, der bestimmt, ob zum Exportieren der Textsprache ein „Span“-Tag in der Dokumentstruktur erstellt werden soll oder nicht.

```csharp
public bool ExportLanguageToSpanTag { get; set; }
```

## Bemerkungen

Der Standardwert ist`FALSCH`und das Attribut „Lang“ wird an eine markierte Inhaltssequenz in einem Seiteninhaltsstream angehängt.

Wenn der Wert`WAHR` Für den Text mit der nicht standardmäßigen Sprache wird das Tag „Span“ erstellt und das Attribut „Lang“ wird an dieses Tag angehängt.

Dieser Wert wird ignoriert, wenn[`ExportDocumentStructure`](../exportdocumentstructure/) Ist`FALSCH` .

## Beispiele

Zeigt, wie ein „Span“-Tag in der Dokumentstruktur erstellt wird, um die Textsprache zu exportieren.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");
builder.Writeln("Hola mundo!");

PdfSaveOptions saveOptions = new PdfSaveOptions
{
    // Beachten Sie: Wenn „ExportDocumentStructure“ falsch ist, wird „ExportLanguageToSpanTag“ ignoriert.
    ExportDocumentStructure = true, ExportLanguageToSpanTag = true
};

doc.Save(ArtifactsDir + "PdfSaveOptions.ExportLanguageToSpanTag.pdf", saveOptions);
```

### Siehe auch

* class [PdfSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
