---
title: HtmlInsertOptions Enum
linktitle: HtmlInsertOptions
articleTitle: HtmlInsertOptions
second_title: Aspose.Words pour .NET
description: Explorez l'énumération Aspose.Words.HtmlInsertOptions pour personnaliser l'insertion HTML avec la méthode InsertHtml, améliorant ainsi l'efficacité du traitement des documents.
type: docs
weight: 3570
url: /fr/net/aspose.words/htmlinsertoptions/
---
## HtmlInsertOptions enumeration

Spécifie les options pour le[`InsertHtml`](../documentbuilder/inserthtml/) méthode.

```csharp
[Flags]
public enum HtmlInsertOptions
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| None | `0` | Utilisez les options par défaut lors de l'insertion de HTML. |
| UseBuilderFormatting | `1` | Utiliser la police et le formatage de paragraphe spécifiés dans[`DocumentBuilder`](../documentbuilder/) comme formatage de base pour le texte inséré à partir de HTML. |
| RemoveLastEmptyParagraph | `2` | Supprimez le paragraphe vide qui est normalement inséré après le code HTML qui se termine par un élément de niveau bloc. |
| PreserveBlocks | `4` | Conserver les propriétés des éléments au niveau du bloc. |

## Exemples

Montre comment permettre de mieux préserver les bordures et les marges vues.

```csharp
const string html = @"
    <html>
        <div style='border:dotted'>
        <div style='border:solid'>
            <p>paragraph 1</p>
            <p>paragraph 2</p>
        </div>
        </div>
    </html>";

// Définissez le nouveau mode d'importation des éléments HTML au niveau du bloc.
HtmlInsertOptions insertOptions = HtmlInsertOptions.PreserveBlocks;

DocumentBuilder builder = new DocumentBuilder();
builder.InsertHtml(html, insertOptions);
builder.Document.Save(ArtifactsDir + "DocumentBuilder.PreserveBlocks.docx");
```

### Voir également

* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)
