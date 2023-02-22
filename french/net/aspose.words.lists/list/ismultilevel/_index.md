---
title: List.IsMultiLevel
second_title: Référence de l'API Aspose.Words pour .NET
description: List propriété. Renvoie true lorsque la liste contient 9 niveaux  faux quand 1 niveau.
type: docs
weight: 40
url: /fr/net/aspose.words.lists/list/ismultilevel/
---
## List.IsMultiLevel property

Renvoie true lorsque la liste contient 9 niveaux ; faux quand 1 niveau.

```csharp
public bool IsMultiLevel { get; }
```

### Remarques

Les listes que vous créez avec Aspose.Words sont toujours des listes à plusieurs niveaux et contiennent 9 niveaux.

Microsoft Word 2003 et versions ultérieures créent toujours des listes à plusieurs niveaux avec 9 niveaux. Mais dans certains documents, créés avec des versions antérieures de Microsoft Word, vous pouvez rencontrer des listes qui n'ont qu'un seul niveau.

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

### Voir également

* class [List](../)
* espace de noms [Aspose.Words.Lists](../../list/)
* Assemblée [Aspose.Words](../../../)


