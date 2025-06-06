---
title: RevisionCollection Class
linktitle: RevisionCollection
articleTitle: RevisionCollection
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.RevisionCollection  gérez efficacement les révisions de documents avec une puissante collection d'objets Revision pour une édition transparente.
type: docs
weight: 5510
url: /fr/net/aspose.words/revisioncollection/
---
## RevisionCollection class

Une collection de[`Revision`](../revision/) objets qui représentent les révisions dans le document.

Pour en savoir plus, visitez le[Suivre les modifications dans un document](https://docs.aspose.com/words/net/track-changes-in-a-document/) article de documentation.

```csharp
public class RevisionCollection : IEnumerable<Revision>
```

## Propriétés

| Nom | La description |
| --- | --- |
| [Count](../../aspose.words/revisioncollection/count/) { get; } | Renvoie le nombre de révisions dans la collection. |
| [Groups](../../aspose.words/revisioncollection/groups/) { get; } | Collection de groupes de révision. |
| [Item](../../aspose.words/revisioncollection/item/) { get; } | Renvoie un[`Revision`](../revision/) à l'index spécifié. |

## Méthodes

| Nom | La description |
| --- | --- |
| [Accept](../../aspose.words/revisioncollection/accept/)(*[IRevisionCriteria](../irevisioncriteria/)*) | Accepte les révisions qui correspondent aux critères spécifiés. |
| [AcceptAll](../../aspose.words/revisioncollection/acceptall/)() | Accepte toutes les révisions de cette collection. |
| [GetEnumerator](../../aspose.words/revisioncollection/getenumerator/)() | Renvoie un objet énumérateur. |
| [Reject](../../aspose.words/revisioncollection/reject/)(*[IRevisionCriteria](../irevisioncriteria/)*) | Rejette les révisions qui correspondent aux critères spécifiés. |
| [RejectAll](../../aspose.words/revisioncollection/rejectall/)() | Rejette toutes les révisions de cette collection. |

## Remarques

Vous ne créez pas d'instances de cette classe directement. Utilisez le[`Revisions`](../document/revisions/) propriété permettant d'obtenir les révisions présentes dans un document.

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

* class [Revision](../revision/)
* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)
