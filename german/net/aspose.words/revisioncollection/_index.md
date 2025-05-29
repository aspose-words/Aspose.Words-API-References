---
title: RevisionCollection Class
linktitle: RevisionCollection
articleTitle: RevisionCollection
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.RevisionCollection – verwalten Sie Dokumentrevisionen effizient mit einer leistungsstarken Sammlung von Revisionsobjekten für nahtlose Bearbeitung.
type: docs
weight: 5510
url: /de/net/aspose.words/revisioncollection/
---
## RevisionCollection class

Eine Sammlung von[`Revision`](../revision/) Objekte, die Revisionen im Dokument darstellen.

Um mehr zu erfahren, besuchen Sie die[Änderungen in einem Dokument verfolgen](https://docs.aspose.com/words/net/track-changes-in-a-document/) Dokumentationsartikel.

```csharp
public class RevisionCollection : IEnumerable<Revision>
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Count](../../aspose.words/revisioncollection/count/) { get; } | Gibt die Anzahl der Revisionen in der Sammlung zurück. |
| [Groups](../../aspose.words/revisioncollection/groups/) { get; } | Sammlung von Revisionsgruppen. |
| [Item](../../aspose.words/revisioncollection/item/) { get; } | Gibt einen[`Revision`](../revision/) am angegebenen Index. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [Accept](../../aspose.words/revisioncollection/accept/)(*[IRevisionCriteria](../irevisioncriteria/)*) | Akzeptiert Revisionen, die den angegebenen Kriterien entsprechen. |
| [AcceptAll](../../aspose.words/revisioncollection/acceptall/)() | Akzeptiert alle Revisionen in dieser Sammlung. |
| [GetEnumerator](../../aspose.words/revisioncollection/getenumerator/)() | Gibt ein Enumeratorobjekt zurück. |
| [Reject](../../aspose.words/revisioncollection/reject/)(*[IRevisionCriteria](../irevisioncriteria/)*) | Lehnt Revisionen ab, die den angegebenen Kriterien entsprechen. |
| [RejectAll](../../aspose.words/revisioncollection/rejectall/)() | Lehnt alle Revisionen in dieser Sammlung ab. |

## Bemerkungen

Sie erstellen keine Instanzen dieser Klasse direkt. Verwenden Sie die[`Revisions`](../document/revisions/) -Eigenschaft, um in einem Dokument vorhandene Revisionen abzurufen.

## Beispiele

Zeigt, wie mit Revisionen in einem Dokument gearbeitet wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Eine normale Bearbeitung des Dokuments gilt nicht als Revision.
builder.Write("This does not count as a revision. ");

Assert.IsFalse(doc.HasRevisions);

// Um unsere Änderungen als Revisionen zu registrieren, müssen wir einen Autor angeben und dann mit der Verfolgung beginnen.
doc.StartTrackRevisions("John Doe", DateTime.Now);

builder.Write("This is revision #1. ");

Assert.IsTrue(doc.HasRevisions);
Assert.AreEqual(1, doc.Revisions.Count);

// Dieses Flag entspricht der Option „Überprüfen“ -> „Verfolgen“ -> „Änderungen nachverfolgen“ in Microsoft Word.
// Die Methode „StartTrackRevisions“ beeinflusst ihren Wert nicht,
// und das Dokument verfolgt Revisionen programmgesteuert, obwohl es den Wert „false“ hat.
// Wenn wir dieses Dokument mit Microsoft Word öffnen, werden Revisionen nicht nachverfolgt.
Assert.IsFalse(doc.TrackRevisions);

// Wir haben mithilfe des Dokumentgenerators Text hinzugefügt, daher handelt es sich bei der ersten Revision um eine Revision vom Einfügungstyp.
Revision revision = doc.Revisions[0];
Assert.AreEqual("John Doe", revision.Author);
Assert.AreEqual("This is revision #1. ", revision.ParentNode.GetText());
Assert.AreEqual(RevisionType.Insertion, revision.RevisionType);
Assert.AreEqual(revision.DateTime.Date, DateTime.Now.Date);
Assert.AreEqual(doc.Revisions.Groups[0], revision.Group);

// Entfernen Sie einen Lauf, um eine Revision vom Löschtyp zu erstellen.
doc.FirstSection.Body.FirstParagraph.Runs[0].Remove();

// Durch das Hinzufügen einer neuen Revision wird diese am Anfang der Revisionssammlung platziert.
Assert.AreEqual(RevisionType.Deletion, doc.Revisions[0].RevisionType);
Assert.AreEqual(2, doc.Revisions.Count);

// Eingefügte Revisionen werden im Dokumenttext angezeigt, noch bevor wir die Revision akzeptieren/ablehnen.
// Durch das Ablehnen der Revision werden ihre Knoten aus dem Textkörper entfernt. Umgekehrt werden Knoten, die Revisionen bilden, gelöscht
// bleiben auch im Dokument, bis wir die Überarbeitung akzeptieren.
Assert.AreEqual("This does not count as a revision. This is revision #1.", doc.GetText().Trim());

// Durch das Akzeptieren der Löschrevision wird der übergeordnete Knoten aus dem Absatztext entfernt
// und entfernen Sie dann die Revision der Sammlung selbst.
doc.Revisions[0].Accept();

Assert.AreEqual(1, doc.Revisions.Count);
Assert.AreEqual("This is revision #1.", doc.GetText().Trim());

builder.Writeln("");
builder.Write("This is revision #2.");

// Verschieben Sie nun den Knoten, um einen verschiebbaren Revisionstyp zu erstellen.
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

// Die verschobene Revision befindet sich jetzt am Index 1. Lehnen Sie die Revision ab, um ihren Inhalt zu verwerfen.
doc.Revisions[1].Reject();

Assert.AreEqual(6, doc.Revisions.Count);
Assert.AreEqual("This is revision #1. \rThis is revision #2.", doc.GetText().Trim());
```

### Siehe auch

* class [Revision](../revision/)
* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)
