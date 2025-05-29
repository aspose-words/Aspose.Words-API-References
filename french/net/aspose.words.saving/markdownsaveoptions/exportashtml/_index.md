---
title: MarkdownSaveOptions.ExportAsHtml
linktitle: ExportAsHtml
articleTitle: ExportAsHtml
second_title: Aspose.Words pour .NET
description: Découvrez comment la propriété MarkdownSaveOptions ExportAsHtml vous permet de personnaliser les éléments HTML pour une exportation Markdown fluide. Optimisez la polyvalence de votre contenu !
type: docs
weight: 30
url: /fr/net/aspose.words.saving/markdownsaveoptions/exportashtml/
---
## MarkdownSaveOptions.ExportAsHtml property

Permet de spécifier les éléments à exporter vers Markdown sous forme de HTML brut. La valeur par défaut estNone .

```csharp
public MarkdownExportAsHtml ExportAsHtml { get; set; }
```

## Exemples

Montre comment exporter un tableau vers Markdown en tant que HTML brut.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Sample table:");

// Créer une table.
builder.InsertCell();
builder.ParagraphFormat.Alignment = ParagraphAlignment.Right;
builder.Write("Cell1");
builder.InsertCell();
builder.ParagraphFormat.Alignment = ParagraphAlignment.Center;
builder.Write("Cell2");

MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
saveOptions.ExportAsHtml = MarkdownExportAsHtml.Tables;

doc.Save(ArtifactsDir + "MarkdownSaveOptions.ExportTableAsHtml.md", saveOptions);
```

### Voir également

* enum [MarkdownExportAsHtml](../../markdownexportashtml/)
* class [MarkdownSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
