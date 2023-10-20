---
title: HeaderFooterCollection Class
linktitle: HeaderFooterCollection
articleTitle: HeaderFooterCollection
second_title: Aspose.Words pour .NET
description: Aspose.Words.HeaderFooterCollection classe. Fournit un accès typé àHeaderFooter nœuds dunSection  en C#.
type: docs
weight: 3110
url: /fr/net/aspose.words/headerfootercollection/
---
## HeaderFooterCollection class

Fournit un accès typé à[`HeaderFooter`](../headerfooter/) nœuds d'un[`Section`](../section/) .

Pour en savoir plus, visitez le[Travailler avec les en-têtes et les pieds de page](https://docs.aspose.com/words/net/working-with-headers-and-footers/) article documentaire.

```csharp
public class HeaderFooterCollection : NodeCollection
```

## Propriétés

| Nom | La description |
| --- | --- |
| [Count](../../aspose.words/nodecollection/count/) { get; } | Obtient le nombre de nœuds dans la collection. |
| [Item](../../aspose.words/headerfootercollection/item/) { get; } | Récupère un[`HeaderFooter`](../headerfooter/) à l'index donné. (3 indexers) |

## Méthodes

| Nom | La description |
| --- | --- |
| [Add](../../aspose.words/nodecollection/add/)(*[Node](../node/)*) | Ajoute un nœud à la fin de la collection. |
| [Clear](../../aspose.words/nodecollection/clear/)() | Supprime tous les nœuds de cette collection et du document. |
| [Contains](../../aspose.words/nodecollection/contains/)(*[Node](../node/)*) | Détermine si un nœud fait partie de la collection. |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator/)() | Fournit une simple itération de style "foreach" sur la collection de nœuds. |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(*[Node](../node/)*) | Renvoie l'index de base zéro du nœud spécifié. |
| [Insert](../../aspose.words/nodecollection/insert/)(*int, [Node](../node/)*) | Insère un nœud dans la collection à l'index spécifié. |
| [LinkToPrevious](../../aspose.words/headerfootercollection/linktoprevious/#linktoprevious_1)(*bool*) | Lie ou dissocie tous les en-têtes et pieds de page aux en-têtes et pieds de page correspondants dans la section précédente. |
| [LinkToPrevious](../../aspose.words/headerfootercollection/linktoprevious/#linktoprevious)(*[HeaderFooterType](../headerfootertype/), bool*) | Lie ou dissocie l'en-tête ou le pied de page spécifié à l'en-tête ou au pied de page correspondant dans la section précédente. |
| [Remove](../../aspose.words/nodecollection/remove/)(*[Node](../node/)*) | Supprime le nœud de la collection et du document. |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(*int*) | Supprime le nœud à l'index spécifié de la collection et du document. |
| [ToArray](../../aspose.words/headerfootercollection/toarray/#toarray)() | Copie tout`En-têteFoorter` s de la collection à une nouvelle gamme de`En-têteFoorter` s. (2 methods) |

## Remarques

Il peut y en avoir au maximum un[`HeaderFooter`](../headerfooter/)

de chaque[`HeaderFooterType`](../headerfootertype/) par [`Section`](../section/) .

[`HeaderFooter`](../headerfooter/) les objets peuvent apparaître dans n’importe quel ordre dans la collection.

## Exemples

Montre comment supprimer tous les pieds de page d’un document.

```csharp
Document doc = new Document(MyDir + "Header and footer types.docx");

// Parcourez chaque section et supprimez les pieds de page de toutes sortes.
foreach (Section section in doc.OfType<Section>())
{
    // Il existe trois types de types de pied de page et d'en-tête.
    // 1 - L'en-tête/pied de page "Premier", qui n'apparaît que sur la première page d'une section.
    HeaderFooter footer = section.HeadersFooters[HeaderFooterType.FooterFirst];
    footer?.Remove();

    // 2 - L'en-tête/pied de page "Primaire", qui apparaît sur les pages impaires.
    footer = section.HeadersFooters[HeaderFooterType.FooterPrimary];
    footer?.Remove();

     // 3 - L'en-tête/pied de page "Pair", qui apparaît sur les pages paires.
    footer = section.HeadersFooters[HeaderFooterType.FooterEven];
    footer?.Remove();

    Assert.AreEqual(0, section.HeadersFooters.Count(hf => !((HeaderFooter)hf).IsHeader));
}

doc.Save(ArtifactsDir + "HeaderFooter.RemoveFooters.docx");
```

Montre comment créer un en-tête et un pied de page.

```csharp
Document doc = new Document();

// Créez un en-tête et ajoutez-y un paragraphe. Le texte de ce paragraphe
// apparaîtra en haut de chaque page de cette section, au-dessus du corps du texte principal.
HeaderFooter header = new HeaderFooter(doc, HeaderFooterType.HeaderPrimary);
doc.FirstSection.HeadersFooters.Add(header);

Paragraph para = header.AppendParagraph("My header.");

Assert.True(header.IsHeader);
Assert.True(para.IsEndOfHeaderFooter);

// Créez un pied de page et ajoutez-y un paragraphe. Le texte de ce paragraphe
// apparaîtra au bas de chaque page de cette section, sous le corps du texte principal.
HeaderFooter footer = new HeaderFooter(doc, HeaderFooterType.FooterPrimary);
doc.FirstSection.HeadersFooters.Add(footer);

para = footer.AppendParagraph("My footer.");

Assert.False(footer.IsHeader);
Assert.True(para.IsEndOfHeaderFooter);

Assert.AreEqual(footer, para.ParentStory);
Assert.AreEqual(footer.ParentSection, para.ParentSection);
Assert.AreEqual(footer.ParentSection, header.ParentSection);

doc.Save(ArtifactsDir + "HeaderFooter.Create.docx");
```

### Voir également

* class [NodeCollection](../nodecollection/)
* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)
