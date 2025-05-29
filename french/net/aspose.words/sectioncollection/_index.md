---
title: SectionCollection Class
linktitle: SectionCollection
articleTitle: SectionCollection
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.SectionCollection, votre solution de référence pour gérer efficacement les sections de documents avec des fonctionnalités puissantes et une grande flexibilité.
type: docs
weight: 6570
url: /fr/net/aspose.words/sectioncollection/
---
## SectionCollection class

Une collection de[`Section`](../section/) objets dans le document.

Pour en savoir plus, visitez le[Travailler avec des sections](https://docs.aspose.com/words/net/working-with-sections/) article de documentation.

```csharp
public class SectionCollection : NodeCollection
```

## Propriétés

| Nom | La description |
| --- | --- |
| [Count](../../aspose.words/nodecollection/count/) { get; } | Obtient le nombre de nœuds dans la collection. |
| [Item](../../aspose.words/sectioncollection/item/) { get; } | Récupère une section à l'index donné. (2 indexers) |

## Méthodes

| Nom | La description |
| --- | --- |
| [Add](../../aspose.words/nodecollection/add/)(*[Node](../node/)*) | Ajoute un nœud à la fin de la collection. |
| [Clear](../../aspose.words/nodecollection/clear/)() | Supprime tous les nœuds de cette collection et du document. |
| [Contains](../../aspose.words/nodecollection/contains/)(*[Node](../node/)*) | Détermine si un nœud est dans la collection. |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator/)() | Fournit une itération simple de style « foreach » sur la collection de nœuds. |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(*[Node](../node/)*) | Renvoie l'index de base zéro du nœud spécifié. |
| [Insert](../../aspose.words/nodecollection/insert/)(*int, [Node](../node/)*) | Insère un nœud dans la collection à l'index spécifié. |
| [Remove](../../aspose.words/nodecollection/remove/)(*[Node](../node/)*) | Supprime le nœud de la collection et du document. |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(*int*) | Supprime le nœud à l'index spécifié de la collection et du document. |
| [ToArray](../../aspose.words/sectioncollection/toarray/#toarray_1)() | Copie toutes les sections de la collection dans un nouveau tableau de sections. (2 methods) |

## Remarques

Un document Microsoft Word peut contenir plusieurs sections. Pour créer une section dans Microsoft Word, sélectionnez la commande Insérer/Saut et sélectionnez un type de saut. Le saut indique si la section commence sur une nouvelle page ou sur la même page.

L'insertion et la suppression de sections par programmation permettent de personnaliser les documents produits lors du publipostage. Si un document doit avoir un contenu différent, ou des parties de contenu différentes, selon certains critères, vous pouvez créer un document maître contenant plusieurs sections et en supprimer certaines avant ou après le publipostage.

## Exemples

Montre comment ajouter et supprimer des sections dans un document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Section 1");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Section 2");

Assert.AreEqual("Section 1\x000cSection 2", doc.GetText().Trim());

// Supprimez la première section du document.
doc.Sections.RemoveAt(0);

Assert.AreEqual("Section 2", doc.GetText().Trim());

// Ajoutez une copie de ce qui est maintenant la première section à la fin du document.
int lastSectionIdx = doc.Sections.Count - 1;
Section newSection = doc.Sections[lastSectionIdx].Clone();
doc.Sections.Add(newSection);

Assert.AreEqual("Section 2\x000cSection 2", doc.GetText().Trim());
```

### Voir également

* class [NodeCollection](../nodecollection/)
* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)
