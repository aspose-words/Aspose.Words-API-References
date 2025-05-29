---
title: MarkdownExportAsHtml Enum
linktitle: MarkdownExportAsHtml
articleTitle: MarkdownExportAsHtml
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.Saving.MarkdownExportAsHtml pour convertir sans effort des éléments Markdown en HTML brut, améliorant ainsi vos options d'exportation de documents.
type: docs
weight: 6020
url: /fr/net/aspose.words.saving/markdownexportashtml/
---
## MarkdownExportAsHtml enumeration

Permet de spécifier les éléments à exporter vers Markdown sous forme de HTML brut.

```csharp
[Flags]
public enum MarkdownExportAsHtml
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| None | `0` | Exportez tous les éléments en utilisant la syntaxe Markdown sans aucun HTML brut. |
| Tables | `1` | Exporter les tableaux au format HTML brut. |

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

* espace de noms [Aspose.Words.Saving](../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../)
