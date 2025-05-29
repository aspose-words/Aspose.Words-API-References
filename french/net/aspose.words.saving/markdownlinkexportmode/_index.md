---
title: MarkdownLinkExportMode Enum
linktitle: MarkdownLinkExportMode
articleTitle: MarkdownLinkExportMode
second_title: Aspose.Words pour .NET
description: Découvrez comment l'énumération Aspose.Words MarkdownLinkExportMode améliore l'exportation de liens dans Markdown, optimisant ainsi votre processus de conversion de documents sans effort.
type: docs
weight: 6030
url: /fr/net/aspose.words.saving/markdownlinkexportmode/
---
## MarkdownLinkExportMode enumeration

Spécifie comment les liens sont exportés vers Markdown.

```csharp
public enum MarkdownLinkExportMode
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Auto | `0` | Détecter automatiquement le mode d'exportation pour chaque lien. |
| Inline | `1` | Exporter tous les liens sous forme de blocs en ligne. |
| Reference | `2` | Exporter tous les liens sous forme de blocs de référence. |

## Exemples

Montre comment les liens seront écrits dans le fichier .md.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertShape(ShapeType.Balloon, 100, 100);

// L'image sera écrite comme référence :
// ![ref1]
//
// [ref1]: aw_ref.001.png
MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
saveOptions.LinkExportMode = MarkdownLinkExportMode.Reference;
doc.Save(ArtifactsDir + "MarkdownSaveOptions.LinkExportMode.Reference.md", saveOptions);

// L'image sera écrite en ligne :
// ![](aw_inline.001.png)
saveOptions.LinkExportMode = MarkdownLinkExportMode.Inline;
doc.Save(ArtifactsDir + "MarkdownSaveOptions.LinkExportMode.Inline.md", saveOptions);
```

### Voir également

* espace de noms [Aspose.Words.Saving](../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../)
