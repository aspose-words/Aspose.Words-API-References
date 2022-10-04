---
title: TabStopCollection
second_title: Référence de l'API Aspose.Words pour .NET
description: Une collection deTabStop./tabstop/objets qui représentent des tabulations personnalisées pour un paragraphe ou un style.
type: docs
weight: 5910
url: /fr/net/aspose.words/tabstopcollection/
---
## TabStopCollection class

Une collection de[`TabStop`](../tabstop/)objets qui représentent des tabulations personnalisées pour un paragraphe ou un style.

```csharp
public class TabStopCollection : InternableComplexAttr
```

## Propriétés

| Nom | La description |
| --- | --- |
| [Count](../../aspose.words/tabstopcollection/count/) { get; } | Obtient le nombre de taquets de tabulation dans la collection. |
| [Item](../../aspose.words/tabstopcollection/item/) { get; } | Obtient un taquet de tabulation à l'index donné. (2 indexers) |

## Méthodes

| Nom | La description |
| --- | --- |
| [Add](../../aspose.words/tabstopcollection/add/#add)(TabStop) | Ajoute ou remplace un taquet de tabulation dans la collection. |
| [Add](../../aspose.words/tabstopcollection/add/#add_1)(double, TabAlignment, TabLeader) | Ajoute ou remplace un taquet de tabulation dans la collection. |
| [After](../../aspose.words/tabstopcollection/after/)(double) | Obtient un premier taquet de tabulation à droite de la position spécifiée. |
| [Before](../../aspose.words/tabstopcollection/before/)(double) | Obtient un premier taquet de tabulation à gauche de la position spécifiée. |
| [Clear](../../aspose.words/tabstopcollection/clear/)() | Supprime toutes les positions de tabulation. |
| override [Equals](../../aspose.words/tabstopcollection/equals/#equals_1)(object) | Détermine si l'objet spécifié est égal en valeur à l'objet actuel. |
| [Equals](../../aspose.words/tabstopcollection/equals/#equals)(TabStopCollection) | Détermine si la TabStopCollection spécifiée est égale en valeur à la TabStopCollection actuelle. |
| override [GetHashCode](../../aspose.words/tabstopcollection/gethashcode/)() | Sert de fonction de hachage pour ce type. |
| [GetIndexByPosition](../../aspose.words/tabstopcollection/getindexbyposition/)(double) | Obtient l'index d'un taquet de tabulation avec la position spécifiée en points. |
| [GetPositionByIndex](../../aspose.words/tabstopcollection/getpositionbyindex/)(int) | Obtient la position (en points) du taquet de tabulation à l'index spécifié. |
| [RemoveByIndex](../../aspose.words/tabstopcollection/removebyindex/)(int) | Supprime un taquet de tabulation à l'index spécifié de la collection. |
| [RemoveByPosition](../../aspose.words/tabstopcollection/removebyposition/)(double) | Supprime un taquet de tabulation à la position spécifiée de la collection. |

### Remarques

Dans les documents Microsoft Word, un taquet de tabulation peut être défini dans les propriétés d'un style de paragraphe ou directement dans les propriétés d'un paragraphe. Un style peut être basé sur un autre style. Par conséquent, l'ensemble complet de taquets de tabulation pour un objet donné est une combinaison de taquets de tabulation définis directement sur cet objet et de taquets de tabulation hérités des styles parents.

Dans Aspose.Words, lorsque vous obtenez un **TabStops** collection pour un paragraphe ou un style, elle ne contient que les taquets de tabulation personnalisés définis directement pour ce paragraphe ou ce style. La collection n'inclut pas les taquets de tabulation définis dans les styles parents ou les taquets de tabulation par défaut.

### Exemples

Montre comment utiliser la collection de taquets de tabulation d'un document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

TabStopCollection tabStops = builder.ParagraphFormat.TabStops;

// 72 points correspond à un "pouce" sur la règle de taquet de Microsoft Word.
tabStops.Add(new TabStop(72.0));
tabStops.Add(new TabStop(432.0, TabAlignment.Right, TabLeader.Dashes));

Assert.AreEqual(2, tabStops.Count);
Assert.IsFalse(tabStops[0].IsClear);
Assert.IsFalse(tabStops[0].Equals(tabStops[1]));

// Chaque caractère "tab" amène le curseur du générateur à l'emplacement du prochain taquet de tabulation.
builder.Writeln("Start\tTab 1\tTab 2");

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

Assert.AreEqual(2, paragraphs.Count);

// Chaque paragraphe obtient sa collection de taquets de tabulation, qui clone ses valeurs à partir de la collection de taquets de tabulation du générateur de document.
Assert.AreEqual(paragraphs[0].ParagraphFormat.TabStops, paragraphs[1].ParagraphFormat.TabStops);
Assert.AreNotSame(paragraphs[0].ParagraphFormat.TabStops, paragraphs[1].ParagraphFormat.TabStops);

// Une collection d'arrêts de tabulation peut nous diriger vers TabStops avant et après certaines positions.
Assert.AreEqual(72.0, tabStops.Before(100.0).Position);
Assert.AreEqual(432.0, tabStops.After(100.0).Position);

// Nous pouvons effacer la collection de taquets de tabulation d'un paragraphe pour revenir au comportement de tabulation par défaut.
paragraphs[1].ParagraphFormat.TabStops.Clear();

Assert.AreEqual(0, paragraphs[1].ParagraphFormat.TabStops.Count);

doc.Save(ArtifactsDir + "TabStopCollection.TabStopCollection.docx");
```

### Voir également

* class [InternableComplexAttr](../internablecomplexattr/)
* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
