---
title: Class Revision
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.Revision classe. Représente une révision modification suivie dans un nœud ou un style de document. UtilisationRevisionType pour vérifier le type de cette révision.
type: docs
weight: 4500
url: /fr/net/aspose.words/revision/
---
## Revision class

Représente une révision (modification suivie) dans un nœud ou un style de document. Utilisation[`RevisionType`](./revisiontype/) pour vérifier le type de cette révision.

```csharp
public class Revision
```

## Propriétés

| Nom | La description |
| --- | --- |
| [Author](../../aspose.words/revision/author/) { get; set; } | Obtient ou définit l'auteur de cette révision. Ne peut pas être une chaîne vide ou null. |
| [DateTime](../../aspose.words/revision/datetime/) { get; set; } | Obtient ou définit la date/heure de cette révision. |
| [Group](../../aspose.words/revision/group/) { get; } | Obtient le groupe de révision. Renvoie null si la révision n'appartient à aucun groupe. |
| [ParentNode](../../aspose.words/revision/parentnode/) { get; } | Obtient le nœud parent immédiat (propriétaire) de cette révision. Cette propriété fonctionnera pour tout type de révision autre queStyleDefinitionChange . |
| [ParentStyle](../../aspose.words/revision/parentstyle/) { get; } | Obtient le style parent immédiat (propriétaire) de cette révision. Cette propriété ne fonctionnera que pour leStyleDefinitionChange type de révision. |
| [RevisionType](../../aspose.words/revision/revisiontype/) { get; } | Obtient le type de cette révision. |

## Méthodes

| Nom | La description |
| --- | --- |
| [Accept](../../aspose.words/revision/accept/)() | Accepte cette révision. |
| [Reject](../../aspose.words/revision/reject/)() | Rejeter cette révision. |

### Exemples

Montre comment travailler avec des révisions dans un document.

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

// Ce drapeau correspond à la "Revue" -> "Suivi" -> Option "Suivre les modifications" dans Microsoft Word.
// La méthode "StartTrackRevisions" n'affecte pas sa valeur,
// et le document suit les révisions par programme bien qu'il ait la valeur "false".
// Si nous ouvrons ce document à l'aide de Microsoft Word, il ne suivra pas les révisions.
Assert.IsFalse(doc.TrackRevisions);

// Nous avons ajouté du texte à l'aide du générateur de documents, donc la première révision est une révision de type insertion.
Revision revision = doc.Revisions[0];
Assert.AreEqual("John Doe", revision.Author);
Assert.AreEqual("This is revision #1. ", revision.ParentNode.GetText());
Assert.AreEqual(RevisionType.Insertion, revision.RevisionType);
Assert.AreEqual(revision.DateTime.Date, DateTime.Now.Date);
Assert.AreEqual(doc.Revisions.Groups[0], revision.Group);

// Supprimer une exécution pour créer une révision de type suppression.
doc.FirstSection.Body.FirstParagraph.Runs[0].Remove();

// L'ajout d'une nouvelle révision la place au début de la collection de révisions.
Assert.AreEqual(RevisionType.Deletion, doc.Revisions[0].RevisionType);
Assert.AreEqual(2, doc.Revisions.Count);

// Les révisions d'insertion apparaissent dans le corps du document avant même que nous acceptions/rejetons la révision.
// Le rejet de la révision supprimera ses nœuds du corps. Inversement, les nœuds qui composent suppriment les révisions
// s'attarde également dans le document jusqu'à ce que nous acceptions la révision.
Assert.AreEqual("This does not count as a revision. This is revision #1.", doc.GetText().Trim());

// Accepter la suppression de la révision supprimera son nœud parent du texte du paragraphe
// puis supprimez la révision de la collection elle-même.
doc.Revisions[0].Accept();

Assert.AreEqual(1, doc.Revisions.Count);
Assert.AreEqual("This is revision #1.", doc.GetText().Trim());

builder.Writeln("");
builder.Write("This is revision #2.");

// Maintenant, déplacez le nœud pour créer un type de révision mobile.
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

// La révision mobile est maintenant à l'index 1. Rejetez la révision pour supprimer son contenu.
doc.Revisions[1].Reject();

Assert.AreEqual(6, doc.Revisions.Count);
Assert.AreEqual("This is revision #1. \rThis is revision #2.", doc.GetText().Trim());
```

### Voir également

* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)


