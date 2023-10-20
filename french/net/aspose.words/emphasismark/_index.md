---
title: EmphasisMark Enum
linktitle: EmphasisMark
articleTitle: EmphasisMark
second_title: Aspose.Words pour .NET
description: Aspose.Words.EmphasisMark énumération. Spécifie les types possibles de marque daccentuation en C#.
type: docs
weight: 1460
url: /fr/net/aspose.words/emphasismark/
---
## EmphasisMark enumeration

Spécifie les types possibles de marque d'accentuation.

```csharp
public enum EmphasisMark
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| None | `0` | Aucune marque d'accentuation. |
| OverSolidCircle | `1` | La marque d'accentuation est un cercle noir plein affiché au-dessus du texte. |
| OverComma | `2` | La marque d'accentuation est une virgule affichée au-dessus du texte. |
| OverWhiteCircle | `3` | La marque d'accentuation est un cercle blanc vide affiché au-dessus du texte. |
| UnderSolidCircle | `4` | La marque d'accentuation est un cercle noir plein affiché sous le texte. |

## Exemples

Montre comment ajouter un caractère supplémentaire rendu au-dessus/en dessous du caractère glyphe.

```csharp
DocumentBuilder builder = new DocumentBuilder();

// Types possibles de marque d'accentuation :
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
