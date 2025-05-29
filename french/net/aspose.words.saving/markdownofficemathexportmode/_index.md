---
title: MarkdownOfficeMathExportMode Enum
linktitle: MarkdownOfficeMathExportMode
articleTitle: MarkdownOfficeMathExportMode
second_title: Aspose.Words pour .NET
description: Découvrez comment Aspose.Words.Saving.MarkdownOfficeMathExportMode améliore l'exportation OfficeMath vers Markdown, garantissant une conversion de documents précise et efficace.
type: docs
weight: 6050
url: /fr/net/aspose.words.saving/markdownofficemathexportmode/
---
## MarkdownOfficeMathExportMode enumeration

Spécifie comment Aspose.Words exporte OfficeMath vers Markdown.

```csharp
public enum MarkdownOfficeMathExportMode
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Text | `0` | Exporter OfficeMath sous forme de texte brut. |
| Image | `1` | Exporter OfficeMath en tant qu'image. |
| MathML | `2` | Exporter OfficeMath au format MathML. |

## Exemples

Montre comment OfficeMath sera écrit dans le document.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
saveOptions.OfficeMathExportMode = MarkdownOfficeMathExportMode.Image;

doc.Save(ArtifactsDir + "MarkdownSaveOptions.OfficeMathExportMode.md", saveOptions);
```

### Voir également

* espace de noms [Aspose.Words.Saving](../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../)
