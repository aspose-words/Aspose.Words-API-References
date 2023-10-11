---
title: ListCollection.AddCopy
second_title: Référence de l'API Aspose.Words pour .NET
description: ListCollection méthode. Crée une nouvelle liste en copiant la liste spécifiée et en lajoutant à la collection de listes dans le document.
type: docs
weight: 50
url: /fr/net/aspose.words.lists/listcollection/addcopy/
---
## ListCollection.AddCopy method

Crée une nouvelle liste en copiant la liste spécifiée et en l'ajoutant à la collection de listes dans le document.

```csharp
public List AddCopy(List srcList)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| srcList | List | La liste des sources à partir de laquelle copier. |

### Return_Value

La liste nouvellement créée.

### Remarques

La liste des sources peut provenir de n’importe quel document. Si la liste source appartient à un autre document, une copie de la liste est créée et ajoutée au document actuel.

Si la liste source est une référence ou une définition d'un style de liste, la liste nouvellement créée n'est pas liée au style de liste d'origine.

### Exemples

Montre comment créer un document avec un échantillon de toutes les listes d'un autre document.

```csharp
public void PrintOutAllLists()
{
    Document srcDoc = new Document(MyDir + "Rendering.docx");

    Document dstDoc = new Document();
    DocumentBuilder builder = new DocumentBuilder(dstDoc);

    foreach (List srcList in srcDoc.Lists)
    {
        List dstList = dstDoc.Lists.AddCopy(srcList);
        AddListSample(builder, dstList);
    }

    dstDoc.Save(ArtifactsDir + "Lists.PrintOutAllLists.docx");
}

private static void AddListSample(DocumentBuilder builder, List list)
{
    builder.Writeln("Sample formatting of list with ListId:" + list.ListId);
    builder.ListFormat.List = list;
    for (int i = 0; i < list.ListLevels.Count; i++)
    {
        builder.ListFormat.ListLevelNumber = i;
        builder.Writeln("Level " + i);
    }

    builder.ListFormat.RemoveNumbers();
    builder.Writeln();
}
```

Montre comment redémarrer la numérotation dans une liste en copiant une liste.

```csharp
Document doc = new Document();

// Une liste nous permet d'organiser et de décorer des ensembles de paragraphes avec des symboles de préfixe et des retraits.
 // Nous pouvons créer des listes imbriquées en augmentant le niveau d'indentation.
 // Nous pouvons commencer et terminer une liste en utilisant la propriété "ListFormat" d'un générateur de documents.
// Chaque paragraphe que nous ajoutons entre le début et la fin d'une liste deviendra un élément de la liste.
// Créez une liste à partir d'un modèle Microsoft Word et personnalisez son premier niveau de liste.
List list1 = doc.Lists.Add(ListTemplate.NumberArabicParenthesis);
list1.ListLevels[0].Font.Color = Color.Red;
list1.ListLevels[0].Alignment = ListLevelAlignment.Right;

// Applique notre liste à certains paragraphes.
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("List 1 starts below:");
builder.ListFormat.List = list1;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

// Nous pouvons ajouter une copie d'une liste existante à la collection de listes du document
// pour créer une liste similaire sans apporter de modifications à l'original.
List list2 = doc.Lists.AddCopy(list1);
list2.ListLevels[0].Font.Color = Color.Blue;
list2.ListLevels[0].StartAt = 10;

// Applique la deuxième liste aux nouveaux paragraphes.
builder.Writeln("List 2 starts below:");
builder.ListFormat.List = list2;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

doc.Save(ArtifactsDir + "Lists.RestartNumberingUsingListCopy.docx");
```

### Voir également

* class [List](../../list/)
* class [ListCollection](../)
* espace de noms [Aspose.Words.Lists](../../listcollection/)
* Assemblée [Aspose.Words](../../../)


