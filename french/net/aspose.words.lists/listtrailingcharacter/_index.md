---
title: ListTrailingCharacter Enum
linktitle: ListTrailingCharacter
articleTitle: ListTrailingCharacter
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.Lists.ListTrailingCharacter pour personnaliser les étiquettes de liste et améliorer la mise en forme des paragraphes pour une présentation de document soignée.
type: docs
weight: 3990
url: /fr/net/aspose.words.lists/listtrailingcharacter/
---
## ListTrailingCharacter enumeration

Spécifie le caractère qui sépare l'étiquette de la liste du texte du paragraphe.

```csharp
public enum ListTrailingCharacter
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Tab | `0` | Un caractère de tabulation est placé entre l'étiquette de la liste et le texte du paragraphe. |
| Space | `1` | Un caractère espace est placé entre l'étiquette de la liste et le texte du paragraphe. |
| Nothing | `2` | Il n'y a pas de caractère séparateur entre l'étiquette de la liste et le texte du paragraphe. |

## Remarques

Utilisé comme valeur pour le[`TrailingCharacter`](../listlevel/trailingcharacter/) propriété.

## Exemples

Montre comment appliquer une mise en forme de liste personnalisée aux paragraphes lors de l'utilisation de DocumentBuilder.

```csharp
Document doc = new Document();

// Une liste nous permet d'organiser et de décorer des ensembles de paragraphes avec des symboles de préfixe et des retraits.
 // Nous pouvons créer des listes imbriquées en augmentant le niveau d'indentation.
 // Nous pouvons commencer et terminer une liste en utilisant la propriété « ListFormat » d'un générateur de documents.
// Chaque paragraphe que nous ajoutons entre le début et la fin d'une liste deviendra un élément de la liste.
// Créez une liste à partir d’un modèle Microsoft Word et personnalisez les deux premiers niveaux de sa liste.
List list = doc.Lists.Add(ListTemplate.NumberDefault);

ListLevel listLevel = list.ListLevels[0];
listLevel.Font.Color = Color.Red;
listLevel.Font.Size = 24;
listLevel.NumberStyle = NumberStyle.OrdinalText;
listLevel.StartAt = 21;
listLevel.NumberFormat = "\x0000";

listLevel.NumberPosition = -36;
listLevel.TextPosition = 144;
listLevel.TabPosition = 144;

listLevel = list.ListLevels[1];
listLevel.Alignment = ListLevelAlignment.Right;
listLevel.NumberStyle = NumberStyle.Bullet;
listLevel.Font.Name = "Wingdings";
listLevel.Font.Color = Color.Blue;
listLevel.Font.Size = 24;

// Cette valeur NumberFormat créera des symboles de liste à puces en forme d'étoile.
listLevel.NumberFormat = "\xf0af";
listLevel.TrailingCharacter = ListTrailingCharacter.Space;
listLevel.NumberPosition = 144;

// Créez des paragraphes et appliquez-leur les deux niveaux de liste de notre formatage de liste personnalisé.
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ListFormat.List = list;
builder.Writeln("The quick brown fox...");
builder.Writeln("The quick brown fox...");

builder.ListFormat.ListIndent();
builder.Writeln("jumped over the lazy dog.");
builder.Writeln("jumped over the lazy dog.");

builder.ListFormat.ListOutdent();
builder.Writeln("The quick brown fox...");

builder.ListFormat.RemoveNumbers();

builder.Document.Save(ArtifactsDir + "Lists.CreateCustomList.docx");
```

### Voir également

* espace de noms [Aspose.Words.Lists](../../aspose.words.lists/)
* Assemblée [Aspose.Words](../../)
