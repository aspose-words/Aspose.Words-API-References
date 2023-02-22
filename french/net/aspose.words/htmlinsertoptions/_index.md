---
title: Enum HtmlInsertOptions
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.HtmlInsertOptions énumération. Spécifie les options pour leInsertHtml méthode.
type: docs
weight: 2960
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
| None | `0` | Utiliser les options par défaut lors de l'insertion de HTML. |
| UseBuilderFormatting | `1` | Utilisez la police et la mise en forme des paragraphes spécifiées dans[`DocumentBuilder`](../documentbuilder/) comme mise en forme de base pour text inséré à partir de HTML. |
| RemoveLastEmptyParagraph | `2` | Supprimez le paragraphe vide qui est normalement inséré après HTML et qui se termine par un élément de niveau bloc. |
| PreserveBlocks | `4` | Préserver les propriétés des éléments de niveau bloc. |

### Voir également

* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)


