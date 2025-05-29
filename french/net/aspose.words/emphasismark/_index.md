---
title: EmphasisMark Enum
linktitle: EmphasisMark
articleTitle: EmphasisMark
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.EmphasisMark, qui propose différents types d'emphase pour améliorer la mise en forme de vos documents. Optimisez l'impact de votre texte dès aujourd'hui !
type: docs
weight: 1870
url: /fr/net/aspose.words/emphasismark/
---
## EmphasisMark enumeration

Spécifie les types possibles de marque d'emphase.

```csharp
public enum EmphasisMark
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| None | `0` | Pas de signe d'emphase. |
| OverSolidCircle | `1` | Le signe d'emphase est un cercle noir uni affiché au-dessus du texte. |
| OverComma | `2` | Le signe d'emphase est une virgule affichée au-dessus du texte. |
| OverWhiteCircle | `3` | Le signe d'emphase est un cercle blanc vide affiché au-dessus du texte. |
| UnderSolidCircle | `4` | Le signe d'emphase est un cercle noir uni affiché sous le texte. |

## Exemples

Montre comment ajouter un caractère supplémentaire rendu au-dessus/en dessous du caractère glyphe.

```csharp
DocumentBuilder builder = new DocumentBuilder();

// Types possibles de marque d'emphase :
// https://apireference.aspose.com/words/net/aspose.words/emphasismark
builder.Font.EmphasisMark = emphasisMark; 

builder.Write("Emphasis text");
builder.Writeln();
builder.Font.ClearFormatting();
builder.Write("Simple text");

builder.Document.Save(ArtifactsDir + "Fonts.SetEmphasisMark.docx");
```

### Voir également

* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)
