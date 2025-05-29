---
title: Document.TrackRevisions
linktitle: TrackRevisions
articleTitle: TrackRevisions
second_title: Aspose.Words für .NET
description: Aktivieren Sie Document TrackRevisions, um Änderungen in Microsoft Word automatisch zu verfolgen und so eine nahtlose Zusammenarbeit und präzise Versionskontrolle sicherzustellen.
type: docs
weight: 450
url: /de/net/aspose.words/document/trackrevisions/
---
## Document.TrackRevisions property

„True“, wenn Änderungen nachverfolgt werden, wenn dieses Dokument in Microsoft Word bearbeitet wird.

```csharp
public bool TrackRevisions { get; set; }
```

## Bemerkungen

Durch das Festlegen dieser Option wird Microsoft Word lediglich angewiesen, die Funktion „Änderungen nachverfolgen“ ein- oder auszuschalten. Diese Eigenschaft hat keine Auswirkungen auf Änderungen am Dokument, die Sie programmgesteuert über Aspose.Words vornehmen.

Wenn Sie Änderungen automatisch verfolgen möchten, wenn sie programmgesteuert von Aspose.Words an diesem Dokument vorgenommen werden, verwenden Sie die[`StartTrackRevisions`](../starttrackrevisions/) Verfahren.

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

* class [Document](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
