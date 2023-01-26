---
title: ListLevel
second_title: Référence de l'API Aspose.Words pour .NET
description: Définit le formatage pour un niveau de liste.
type: docs
weight: 3300
url: /fr/net/aspose.words.lists/listlevel/
---
## ListLevel class

Définit le formatage pour un niveau de liste.

```csharp
public class ListLevel
```

## Propriétés

| Nom | La description |
| --- | --- |
| [Alignment](../../aspose.words.lists/listlevel/alignment/) { get; set; } | Obtient ou définit la justification du numéro réel de l'élément de liste. |
| [CustomNumberStyleFormat](../../aspose.words.lists/listlevel/customnumberstyleformat/) { get; } | Obtient le format de style de nombre personnalisé pour ce niveau de liste. Par exemple : "a, ç, ĝ, ...". |
| [Font](../../aspose.words.lists/listlevel/font/) { get; } | Spécifie le formatage des caractères utilisé pour l'étiquette de la liste. |
| [ImageData](../../aspose.words.lists/listlevel/imagedata/) { get; } | Renvoie les données d'image de la forme de puce d'image pour le niveau de liste actuel. |
| [IsLegal](../../aspose.words.lists/listlevel/islegal/) { get; set; } | Vrai si le niveau transforme tous les nombres hérités en arabe, faux s'il conserve leur style de nombre. |
| [LinkedStyle](../../aspose.words.lists/listlevel/linkedstyle/) { get; set; } | Obtient ou définit le style de paragraphe lié à ce niveau de liste. |
| [NumberFormat](../../aspose.words.lists/listlevel/numberformat/) { get; set; } | Renvoie ou définit le format numérique pour le niveau de liste. |
| [NumberPosition](../../aspose.words.lists/listlevel/numberposition/) { get; set; } | Renvoie ou définit la position (en points) du numéro ou de la puce pour le niveau de liste. |
| [NumberStyle](../../aspose.words.lists/listlevel/numberstyle/) { get; set; } | Renvoie ou définit le style de numérotation pour ce niveau de liste. |
| [RestartAfterLevel](../../aspose.words.lists/listlevel/restartafterlevel/) { get; set; } | Définit ou renvoie le niveau de liste qui doit apparaître avant que le niveau de liste spécifié ne redémarre la numérotation. |
| [StartAt](../../aspose.words.lists/listlevel/startat/) { get; set; } | Renvoie ou définit le numéro de départ pour ce niveau de liste. |
| [TabPosition](../../aspose.words.lists/listlevel/tabposition/) { get; set; } | Renvoie ou définit la position de tabulation (en points) pour le niveau de liste. |
| [TextPosition](../../aspose.words.lists/listlevel/textposition/) { get; set; } | Renvoie ou définit la position (en points) de la deuxième ligne de texte d'habillage pour le niveau de liste. |
| [TrailingCharacter](../../aspose.words.lists/listlevel/trailingcharacter/) { get; set; } | Renvoie ou définit le caractère inséré après le numéro pour le niveau de liste. |

## Méthodes

| Nom | La description |
| --- | --- |
| [CreatePictureBullet](../../aspose.words.lists/listlevel/createpicturebullet/)() | Crée une forme de puce d'image pour le niveau de liste actuel. |
| [DeletePictureBullet](../../aspose.words.lists/listlevel/deletepicturebullet/)() | Supprime la puce d'image pour le niveau de liste actuel. |
| [Equals](../../aspose.words.lists/listlevel/equals/#equals)(ListLevel) | Compare avec le ListLevel. spécifié |
| override [GetHashCode](../../aspose.words.lists/listlevel/gethashcode/)() | Calcule le code de hachage pour cet objet. |
| static [GetEffectiveValue](../../aspose.words.lists/listlevel/geteffectivevalue/)(int, NumberStyle, string) | Indique la représentation sous forme de chaîne du`ListLevel` objet pour l'index spécifié de l'élément de liste. Les paramètres spécifient le[`NumberStyle`](../../aspose.words/numberstyle/) et un format optionnel string utilisé lorsqueCustom est spécifié. |

### Remarques

Vous ne créez pas d'objets de cette classe. Les objets de niveau liste sont créés automatiquement lors de la création d'une liste. Vous accédez`ListLevel` objets via the [`ListLevelCollection`](../listlevelcollection/) le recueil.

Utilisez les propriétés de`ListLevel` pour spécifier le formatage de liste pour les niveaux de liste individuels.

### Exemples

Montre comment appliquer une mise en forme de liste personnalisée aux paragraphes lors de l'utilisation de DocumentBuilder.

```csharp
Document doc = new Document();

// Une liste nous permet d'organiser et de décorer des ensembles de paragraphes avec des symboles de préfixe et des retraits.
// Nous pouvons créer des listes imbriquées en augmentant le niveau d'indentation. 
// Nous pouvons commencer et terminer une liste en utilisant la propriété "ListFormat" d'un générateur de document. 
// Chaque paragraphe que nous ajoutons entre le début et la fin d'une liste deviendra un élément de la liste.
// Crée une liste à partir d'un modèle Microsoft Word et personnalise les deux premiers de ses niveaux de liste.
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

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
