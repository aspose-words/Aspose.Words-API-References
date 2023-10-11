---
title: ListCollection.Add
second_title: Référence de l'API Aspose.Words pour .NET
description: ListCollection méthode. Crée une nouvelle liste basée sur un modèle prédéfini et lajoute à la collection de listes du document.
type: docs
weight: 40
url: /fr/net/aspose.words.lists/listcollection/add/
---
## Add(ListTemplate) {#add}

Crée une nouvelle liste basée sur un modèle prédéfini et l'ajoute à la collection de listes du document.

```csharp
public List Add(ListTemplate listTemplate)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| listTemplate | ListTemplate | Le modèle de la liste. |

### Return_Value

La liste nouvellement créée.

### Remarques

Les modèles de liste Aspose.Words correspondent aux 21 modèles de liste disponibles dans la boîte de dialogue Puces et numérotation de Microsoft Word 2003.

Toutes les listes créées à l'aide de cette méthode comportent 9 niveaux de liste.

### Exemples

Montre comment créer une liste en appliquant un nouveau format de liste à une collection de paragraphes.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Paragraph 1");
builder.Writeln("Paragraph 2");
builder.Write("Paragraph 3");

NodeCollection paras = doc.GetChildNodes(NodeType.Paragraph, true);

Assert.AreEqual(0, paras.Count(n => (n as Paragraph).ListFormat.IsListItem));

List list = doc.Lists.Add(ListTemplate.NumberUppercaseLetterDot);

foreach (Paragraph paragraph in paras.OfType<Paragraph>())
{
    paragraph.ListFormat.List = list;
    paragraph.ListFormat.ListLevelNumber = 1;
}

Assert.AreEqual(3, paras.Count(n => (n as Paragraph).ListFormat.IsListItem));
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

* class [List](../../list/)
* enum [ListTemplate](../../listtemplate/)
* class [ListCollection](../)
* espace de noms [Aspose.Words.Lists](../../listcollection/)
* Assemblée [Aspose.Words](../../../)

---

## Add(Style) {#add_1}

Crée une nouvelle liste qui fait référence à un style de liste et l'ajoute à la collection de listes dans le document.

```csharp
public List Add(Style listStyle)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| listStyle | Style | Le style de liste. |

### Return_Value

La liste nouvellement créée.

### Remarques

La liste nouvellement créée fait référence au style de liste. Si vous modifiez les propriétés du style list , cela se reflète dans les propriétés de la liste. Vice versa, si vous modifiez les propriétés de la liste, cela se reflète dans les propriétés du style de liste.

### Exemples

Montre comment créer un style de liste et l’utiliser dans un document.

```csharp
Document doc = new Document();

// Une liste nous permet d'organiser et de décorer des ensembles de paragraphes avec des symboles de préfixe et des retraits.
 // Nous pouvons créer des listes imbriquées en augmentant le niveau d'indentation.
 // Nous pouvons commencer et terminer une liste en utilisant la propriété "ListFormat" d'un générateur de documents.
// Chaque paragraphe que nous ajoutons entre le début et la fin d'une liste deviendra un élément de la liste.
// Nous pouvons contenir un objet List entier dans un style.
Style listStyle = doc.Styles.Add(StyleType.List, "MyListStyle");

List list1 = listStyle.List;

Assert.True(list1.IsListStyleDefinition);
Assert.False(list1.IsListStyleReference);
Assert.True(list1.IsMultiLevel);
Assert.AreEqual(listStyle, list1.Style);

// Change l'apparence de tous les niveaux de liste dans notre liste.
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

// Ajoutez quelques éléments de liste que notre liste formatera.
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

* class [List](../../list/)
* class [Style](../../../aspose.words/style/)
* class [ListCollection](../)
* espace de noms [Aspose.Words.Lists](../../listcollection/)
* Assemblée [Aspose.Words](../../../)


