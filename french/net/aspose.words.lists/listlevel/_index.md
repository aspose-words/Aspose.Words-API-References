---
title: ListLevel Class
linktitle: ListLevel
articleTitle: ListLevel
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.Lists.ListLevel pour une mise en forme avancée des listes. Améliorez la structure de votre document grâce à des options puissantes et personnalisables.
type: docs
weight: 3950
url: /fr/net/aspose.words.lists/listlevel/
---
## ListLevel class

Définit le formatage pour un niveau de liste.

Pour en savoir plus, visitez le[Travailler avec des listes](https://docs.aspose.com/words/net/working-with-lists/) article de documentation.

```csharp
public class ListLevel
```

## Propriétés

| Nom | La description |
| --- | --- |
| [Alignment](../../aspose.words.lists/listlevel/alignment/) { get; set; } | Obtient ou définit la justification du nombre réel de l'élément de la liste. |
| [CustomNumberStyleFormat](../../aspose.words.lists/listlevel/customnumberstyleformat/) { get; set; } | Récupère ou définit le format de style de nombre personnalisé pour ce niveau de liste. Par exemple : « a, ç, ĝ, ... ». |
| [Font](../../aspose.words.lists/listlevel/font/) { get; } | Spécifie le formatage des caractères utilisé pour l'étiquette de la liste. |
| [ImageData](../../aspose.words.lists/listlevel/imagedata/) { get; } | Renvoie les données d'image de la forme de puce d'image pour le niveau de liste actuel. |
| [IsLegal](../../aspose.words.lists/listlevel/islegal/) { get; set; } | Vrai si le niveau transforme tous les nombres hérités en arabe, faux s'il conserve leur style numérique. |
| [LinkedStyle](../../aspose.words.lists/listlevel/linkedstyle/) { get; set; } | Obtient ou définit le style de paragraphe lié à ce niveau de liste. |
| [NumberFormat](../../aspose.words.lists/listlevel/numberformat/) { get; set; } | Renvoie ou définit le format numérique pour le niveau de liste. |
| [NumberPosition](../../aspose.words.lists/listlevel/numberposition/) { get; set; } | Renvoie ou définit la position (en points) du numéro ou de la puce pour le niveau de liste. |
| [NumberStyle](../../aspose.words.lists/listlevel/numberstyle/) { get; set; } | Renvoie ou définit le style de numéro pour ce niveau de liste. |
| [RestartAfterLevel](../../aspose.words.lists/listlevel/restartafterlevel/) { get; set; } | Définit ou renvoie le niveau de liste qui doit apparaître avant que le niveau de liste spécifié ne redémarre la numérotation. |
| [StartAt](../../aspose.words.lists/listlevel/startat/) { get; set; } | Renvoie ou définit le numéro de départ de ce niveau de liste. |
| [TabPosition](../../aspose.words.lists/listlevel/tabposition/) { get; set; } | Renvoie ou définit la position de tabulation (en points) pour le niveau de liste. |
| [TextPosition](../../aspose.words.lists/listlevel/textposition/) { get; set; } | Renvoie ou définit la position (en points) de la deuxième ligne de texte d'habillage pour le niveau de liste. |
| [TrailingCharacter](../../aspose.words.lists/listlevel/trailingcharacter/) { get; set; } | Renvoie ou définit le caractère inséré après le numéro pour le niveau de liste. |

## Méthodes

| Nom | La description |
| --- | --- |
| [CreatePictureBullet](../../aspose.words.lists/listlevel/createpicturebullet/)() | Crée une forme de puce d'image pour le niveau de liste actuel. |
| [DeletePictureBullet](../../aspose.words.lists/listlevel/deletepicturebullet/)() | Supprime la puce d'image pour le niveau de liste actuel. |
| [Equals](../../aspose.words.lists/listlevel/equals/#equals)(*ListLevel*) | Compare avec le ListLevel spécifié. |
| override [GetHashCode](../../aspose.words.lists/listlevel/gethashcode/)() | Calcule le code de hachage pour cet objet. |
| static [GetEffectiveValue](../../aspose.words.lists/listlevel/geteffectivevalue/)(*int, [NumberStyle](../../aspose.words/numberstyle/), string*) | Indique la représentation sous forme de chaîne de`ListLevel`objet pour l'index spécifié de l'élément de liste. Les paramètres spécifient[`NumberStyle`](../../aspose.words/numberstyle/) et une chaîne de format facultative utilisée lorsqueCustom est spécifié. |

## Remarques

Vous ne créez pas d'objets de cette classe. Les objets de niveau liste sont créés automatiquement lors de la création d'une liste. Vous accédez`ListLevel` objets via the [`ListLevelCollection`](../listlevelcollection/) collection.

Utiliser les propriétés de`ListLevel` pour spécifier le formatage de la liste pour les niveaux de liste individuels.

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
