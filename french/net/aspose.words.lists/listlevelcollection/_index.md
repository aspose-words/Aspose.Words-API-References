---
title: Class ListLevelCollection
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.Lists.ListLevelCollection classe. Une collection de mise en forme de liste pour chaque niveau dans une liste.
type: docs
weight: 3320
url: /fr/net/aspose.words.lists/listlevelcollection/
---
## ListLevelCollection class

Une collection de mise en forme de liste pour chaque niveau dans une liste.

```csharp
public class ListLevelCollection : IEnumerable<ListLevel>
```

## Propriétés

| Nom | La description |
| --- | --- |
| [Count](../../aspose.words.lists/listlevelcollection/count/) { get; } | Obtient le nombre de niveaux dans cette liste. |
| [Item](../../aspose.words.lists/listlevelcollection/item/) { get; set; } | Obtient un niveau de liste par index. |

## Méthodes

| Nom | La description |
| --- | --- |
| [GetEnumerator](../../aspose.words.lists/listlevelcollection/getenumerator/)() | Obtient l'objet énumérateur qui énumérera les niveaux de cette liste. |

### Exemples

Montre comment créer un style de liste et l'utiliser dans un document.

```csharp
Document doc = new Document();

// Une liste nous permet d'organiser et de décorer des ensembles de paragraphes avec des symboles de préfixe et des retraits.
// Nous pouvons créer des listes imbriquées en augmentant le niveau d'indentation. 
// Nous pouvons commencer et terminer une liste en utilisant la propriété "ListFormat" d'un générateur de document. 
// Chaque paragraphe que nous ajoutons entre le début et la fin d'une liste deviendra un élément de la liste.
// Nous pouvons contenir un objet List entier dans un style.
Style listStyle = doc.Styles.Add(StyleType.List, "MyListStyle");

List list1 = listStyle.List;

Assert.True(list1.IsListStyleDefinition);
Assert.False(list1.IsListStyleReference);
Assert.True(list1.IsMultiLevel);
Assert.AreEqual(listStyle, list1.Style);

// Modifie l'apparence de tous les niveaux de liste dans notre liste.
foreach (ListLevel level in list1.ListLevels)
{
    level.Font.Name = "Verdana";
    level.Font.Color = Color.Blue;
    level.Font.Bold = true;
}

DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Using list style first time:");

// Crée une autre liste à partir d'une liste dans un style.
List list2 = doc.Lists.Add(listStyle);

Assert.False(list2.IsListStyleDefinition);
Assert.True(list2.IsListStyleReference);
Assert.AreEqual(listStyle, list2.Style);

// Ajoutez des éléments de liste que notre liste formatera.
builder.ListFormat.List = list2;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

builder.Writeln("Using list style second time:");

// Crée et applique une autre liste basée sur le style de liste.
List list3 = doc.Lists.Add(listStyle);
builder.ListFormat.List = list3;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

builder.Document.Save(ArtifactsDir + "Lists.CreateAndUseListStyle.docx");
```

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

* class [ListLevel](../listlevel/)
* espace de noms [Aspose.Words.Lists](../../aspose.words.lists/)
* Assemblée [Aspose.Words](../../)


