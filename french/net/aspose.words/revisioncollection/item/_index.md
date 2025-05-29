---
title: RevisionCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words pour .NET
description: Accédez facilement à des révisions spécifiques grâce à la propriété d'élément RevisionCollection. Récupérez rapidement les révisions par index pour une gestion simplifiée des données.
type: docs
weight: 30
url: /fr/net/aspose.words/revisioncollection/item/
---
## RevisionCollection indexer

Renvoie un[`Revision`](../../revision/) à l'index spécifié.

```csharp
public Revision this[int index] { get; }
```

| Paramètre | La description |
| --- | --- |
| index | Un index de la collection. |

## Remarques

L'indice est basé sur zéro.

Les index négatifs sont autorisés et indiquent l'accès depuis l'arrière de la collection. Par exemple, -1 signifie le dernier élément, -2 signifie l'avant-dernier et ainsi de suite.

Si l'index est supérieur ou égal au nombre d'éléments dans la liste, cela renvoie une référence nulle.

Si l'index est négatif et que sa valeur absolue est supérieure au nombre d'éléments dans la liste, cela renvoie une référence nulle.

## Exemples

Montre comment travailler avec les révisions dans un document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// L'édition normale du document ne compte pas comme une révision.
builder.Write("This does not count as a revision. ");

Assert.IsFalse(doc.HasRevisions);

// Pour enregistrer nos modifications en tant que révisions, nous devons déclarer un auteur, puis commencer à les suivre.
doc.StartTrackRevisions("John Doe", DateTime.Now);

builder.Write("This is revision #1. ");

Assert.IsTrue(doc.HasRevisions);
Assert.AreEqual(1, doc.Revisions.Count);

// Cet indicateur correspond à l'option « Révision » -> « Suivi » -> « Suivi des modifications » dans Microsoft Word.
// La méthode "StartTrackRevisions" n'affecte pas sa valeur,
// et le document suit les révisions par programmation malgré sa valeur « false ».
// Si nous ouvrons ce document à l'aide de Microsoft Word, il ne suivra pas les révisions.
Assert.IsFalse(doc.TrackRevisions);

// Nous avons ajouté du texte à l'aide du générateur de documents, donc la première révision est une révision de type insertion.
Revision revision = doc.Revisions[0];
Assert.AreEqual("John Doe", revision.Author);
Assert.AreEqual("This is revision #1. ", revision.ParentNode.GetText());
Assert.AreEqual(RevisionType.Insertion, revision.RevisionType);
Assert.AreEqual(revision.DateTime.Date, DateTime.Now.Date);
Assert.AreEqual(doc.Revisions.Groups[0], revision.Group);

// Supprimez une exécution pour créer une révision de type suppression.
doc.FirstSection.Body.FirstParagraph.Runs[0].Remove();

// L'ajout d'une nouvelle révision la place au début de la collection de révisions.
Assert.AreEqual(RevisionType.Deletion, doc.Revisions[0].RevisionType);
Assert.AreEqual(2, doc.Revisions.Count);

// Les révisions d'insertion apparaissent dans le corps du document avant même que nous acceptions/rejetions la révision.
// Rejeter la révision supprimera ses nœuds du corps. À l'inverse, les nœuds qui la composent suppriment les révisions.
// restent également dans le document jusqu'à ce que nous acceptions la révision.
Assert.AreEqual("This does not count as a revision. This is revision #1.", doc.GetText().Trim());

// L'acceptation de la suppression de révision supprimera son nœud parent du texte du paragraphe
// puis supprimez la révision de la collection elle-même.
doc.Revisions[0].Accept();

Assert.AreEqual(1, doc.Revisions.Count);
Assert.AreEqual("This is revision #1.", doc.GetText().Trim());

builder.Writeln("");
builder.Write("This is revision #2.");

// Déplacez maintenant le nœud pour créer un type de révision mobile.
Node node = doc.FirstSection.Body.Paragraphs[1];
Node endNode = doc.FirstSection.Body.Paragraphs[1].NextSibling;
Node referenceNode = doc.FirstSection.Body.Paragraphs[0];

while (node != endNode)
{
    Node nextNode = node.NextSibling;
    doc.FirstSection.Body.InsertBefore(node, referenceNode);
    node = nextNode;
}

Assert.AreEqual(RevisionType.Moving, doc.Revisions[0].RevisionType);
Assert.AreEqual(8, doc.Revisions.Count);
Assert.AreEqual("This is revision #2.\rThis is revision #1. \rThis is revision #2.", doc.GetText().Trim());

// La révision en mouvement est maintenant à l'index 1. Rejetez la révision pour supprimer son contenu.
doc.Revisions[1].Reject();

Assert.AreEqual(6, doc.Revisions.Count);
Assert.AreEqual("This is revision #1. \rThis is revision #2.", doc.GetText().Trim());
```

### Voir également

* class [Revision](../../revision/)
* class [RevisionCollection](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
