---
title: Class ListCollection
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.Lists.ListCollection classe. Stocke et gère le formatage des listes à puces et numérotées utilisées dans un document.
type: docs
weight: 3470
url: /fr/net/aspose.words.lists/listcollection/
---
## ListCollection class

Stocke et gère le formatage des listes à puces et numérotées utilisées dans un document.

Pour en savoir plus, visitez le[Travailler avec des listes](https://docs.aspose.com/words/net/working-with-lists/) article documentaire.

```csharp
public class ListCollection : IEnumerable<List>
```

## Propriétés

| Nom | La description |
| --- | --- |
| [Count](../../aspose.words.lists/listcollection/count/) { get; } | Obtient le nombre de listes numérotées et à puces dans le document. |
| [Document](../../aspose.words.lists/listcollection/document/) { get; } | Obtient le document propriétaire. |
| [Item](../../aspose.words.lists/listcollection/item/) { get; } | Obtient une liste par index. |

## Méthodes

| Nom | La description |
| --- | --- |
| [Add](../../aspose.words.lists/listcollection/add/#add)(ListTemplate) | Crée une nouvelle liste basée sur un modèle prédéfini et l'ajoute à la collection de listes du document. |
| [Add](../../aspose.words.lists/listcollection/add/#add_1)(Style) | Crée une nouvelle liste qui fait référence à un style de liste et l'ajoute à la collection de listes dans le document. |
| [AddCopy](../../aspose.words.lists/listcollection/addcopy/)(List) | Crée une nouvelle liste en copiant la liste spécifiée et en l'ajoutant à la collection de listes dans le document. |
| [GetEnumerator](../../aspose.words.lists/listcollection/getenumerator/)() | Obtient l'objet énumérateur qui énumérera les listes dans le document. |
| [GetListByListId](../../aspose.words.lists/listcollection/getlistbylistid/)(int) | Obtient une liste par un identifiant de liste. |

### Remarques

Une liste dans un document Microsoft Word est un ensemble de propriétés de formatage de liste. Le formatage des listes est stocké dans le`ListCollection` collection séparément des paragraphes de texte.

Vous ne créez pas d'objets de cette classe. Il n'y en a toujours qu'un`ListCollection` objet par document et il est accessible via le[`Lists`](../../aspose.words/documentbase/lists/) propriété.

Pour créer une nouvelle liste basée sur un modèle de liste prédéfini ou basée sur un style de liste, utilisez le[`Add`](./add/) méthode.

Pour créer une nouvelle liste avec un formatage identique à une liste existante, utilisez le[`AddCopy`](./addcopy/) méthode.

Pour créer un paragraphe à puces ou numéroté, vous devez appliquer list formatting à un paragraphe en attribuant un[`List`](../list/)objet à the [`List`](../listformat/list/) propriété de[`ListFormat`](../listformat/).

Pour supprimer la mise en forme de liste d'un paragraphe, utilisez l'option[`RemoveNumbers`](../listformat/removenumbers/) Méthode .

Si vous connaissez un peu WordprocessingML, vous savez peut-être qu'il définit des concepts distincts pour "liste" et "définition de liste". Cela correspond exactement à la façon dont le formatage de liste est stocké dans un document Microsoft Word de bas niveau. La définition de liste est comme un "schéma" et la liste est comme une instance d'une définition de liste.

Pour simplifier le modèle de programmation, Aspose.Words masque la distinction entre la définition de list et list de la même manière que Microsoft Word la cache dans son interface utilisateur. Cela vous permet de vous concentrer davantage sur l'apparence de votre document, plutôt que sur . créer des objets de bas niveau pour satisfaire aux exigences du format de fichier Microsoft Word.

Il n'est pas possible de supprimer des listes une fois qu'elles sont créées dans la version actuelle d'Aspose.Words. . Ceci est similaire à Microsoft Word où l'utilisateur n'a pas de contrôle explicite sur les définitions de liste.

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

Montre comment utiliser les niveaux de liste.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Assert.False(builder.ListFormat.IsListItem);

// Une liste nous permet d'organiser et de décorer des ensembles de paragraphes avec des symboles de préfixe et des retraits.
 // Nous pouvons créer des listes imbriquées en augmentant le niveau d'indentation.
 // Nous pouvons commencer et terminer une liste en utilisant la propriété "ListFormat" d'un générateur de documents.
// Chaque paragraphe que nous ajoutons entre le début et la fin d'une liste deviendra un élément de la liste.
// Vous trouverez ci-dessous deux types de listes que nous pouvons créer à l'aide d'un générateur de documents.
// 1 - Une liste numérotée :
// Les listes numérotées créent un ordre logique pour leurs paragraphes en numérotant chaque élément.
builder.ListFormat.List = doc.Lists.Add(ListTemplate.NumberDefault);

Assert.True(builder.ListFormat.IsListItem);

// En définissant la propriété "ListLevelNumber", nous pouvons augmenter le niveau de la liste
// pour commencer une sous-liste autonome à l'élément de liste actuel.
// Le modèle de liste Microsoft Word appelé « NumberDefault » utilise des nombres pour créer des niveaux de liste pour le premier niveau de liste.
 // Les niveaux de liste plus profonds utilisent des lettres et des chiffres romains minuscules.
for (int i = 0; i < 9; i++)
{
    builder.ListFormat.ListLevelNumber = i;
    builder.Writeln("Level " + i);
}

// 2 - Une liste à puces :
// Cette liste appliquera un retrait et une puce ("•") avant chaque paragraphe.
// Les niveaux plus profonds de cette liste utiliseront différents symboles, tels que " ■ " et " ○ ".
builder.ListFormat.List = doc.Lists.Add(ListTemplate.BulletDefault);

for (int i = 0; i < 9; i++)
{
    builder.ListFormat.ListLevelNumber = i;
    builder.Writeln("Level " + i);
}

// Nous pouvons désactiver le formatage de la liste pour ne pas formater les paragraphes suivants sous forme de listes en désactivant l'indicateur "Liste".
builder.ListFormat.List = null;

Assert.False(builder.ListFormat.IsListItem);

doc.Save(ArtifactsDir + "Lists.SpecifyListLevel.docx");
```

### Voir également

* class [List](../list/)
* espace de noms [Aspose.Words.Lists](../../aspose.words.lists/)
* Assemblée [Aspose.Words](../../)


