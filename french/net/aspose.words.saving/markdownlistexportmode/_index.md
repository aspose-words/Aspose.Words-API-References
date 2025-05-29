---
title: MarkdownListExportMode Enum
linktitle: MarkdownListExportMode
articleTitle: MarkdownListExportMode
second_title: Aspose.Words pour .NET
description: Découvrez comment l'énumération MarkdownListExportMode d'Aspose.Words améliore l'exportation de listes vers Markdown, garantissant un formatage précis et une intégration transparente pour vos documents.
type: docs
weight: 6040
url: /fr/net/aspose.words.saving/markdownlistexportmode/
---
## MarkdownListExportMode enumeration

Spécifie comment les listes sont exportées vers Markdown.

```csharp
public enum MarkdownListExportMode
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| MarkdownSyntax | `0` | Exporter les éléments de la liste compatibles avec la syntaxe Markdown. |
| PlainText | `1` | Exporter les éléments de la liste sous forme de texte brut. |

## Exemples

Montre comment les éléments de la liste seront écrits dans le document Markdown.

```csharp
Document doc = new Document(MyDir + "List item.docx");

// Utilisez MarkdownListExportMode.PlainText ou MarkdownListExportMode.MarkdownSyntax pour exporter la liste.
MarkdownSaveOptions options = new MarkdownSaveOptions { ListExportMode = markdownListExportMode };
doc.Save(ArtifactsDir + "MarkdownSaveOptions.ListExportMode.md", options);
```

### Voir également

* espace de noms [Aspose.Words.Saving](../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../)
