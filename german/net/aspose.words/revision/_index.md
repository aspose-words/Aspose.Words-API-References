---
title: Class Revision
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Revision klas. Stellt eine Revision nachverfolgte Änderung in einem Dokumentknoten oder stil dar. VerwendungRevisionType um den Typ dieser Revision zu überprüfen.
type: docs
weight: 4760
url: /de/net/aspose.words/revision/
---
## Revision class

Stellt eine Revision (nachverfolgte Änderung) in einem Dokumentknoten oder -stil dar. Verwendung[`RevisionType`](./revisiontype/) um den Typ dieser Revision zu überprüfen.

Um mehr zu erfahren, besuchen Sie die[Verfolgen Sie Änderungen in einem Dokument](https://docs.aspose.com/words/net/track-changes-in-a-document/) Dokumentationsartikel.

```csharp
public class Revision
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Author](../../aspose.words/revision/author/) { get; set; } | Ruft den Autor dieser Revision ab oder legt ihn fest. Darf keine leere Zeichenfolge oder sein`Null` . |
| [DateTime](../../aspose.words/revision/datetime/) { get; set; } | Ruft das Datum/die Uhrzeit dieser Revision ab oder legt diese fest. |
| [Group](../../aspose.words/revision/group/) { get; } | Ruft die Revisionsgruppe ab. Kehrt zurück`Null` wenn die Revision zu keiner Gruppe gehört. |
| [ParentNode](../../aspose.words/revision/parentnode/) { get; } | Ruft den unmittelbar übergeordneten Knoten (Eigentümer) dieser Revision ab. Diese Eigenschaft funktioniert für jeden Revisionstyp außerStyleDefinitionChange . |
| [ParentStyle](../../aspose.words/revision/parentstyle/) { get; } | Ruft den unmittelbaren übergeordneten Stil (Eigentümer) dieser Revision ab. Diese Eigenschaft funktioniert nur fürStyleDefinitionChange Revisionstyp. |
| [RevisionType](../../aspose.words/revision/revisiontype/) { get; } | Ruft den Typ dieser Revision ab. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [Accept](../../aspose.words/revision/accept/)() | Akzeptiert diese Revision. |
| [Reject](../../aspose.words/revision/reject/)() | Diese Überarbeitung ablehnen. |

### Beispiele

Zeigt, wie mit Revisionen in einem Dokument gearbeitet wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Eine normale Bearbeitung des Dokuments gilt nicht als Überarbeitung.
builder.Write("This does not count as a revision. ");

Assert.IsFalse(doc.HasRevisions);

// Um unsere Änderungen als Überarbeitungen zu registrieren, müssen wir einen Autor deklarieren und dann mit der Verfolgung beginnen.
doc.StartTrackRevisions("John Doe", DateTime.Now);

builder.Write("This is revision #1. ");

Assert.IsTrue(doc.HasRevisions);
Assert.AreEqual(1, doc.Revisions.Count);

// Dieses Flag entspricht dem „Review“ -> „Tracking“ -> Option „Änderungen verfolgen“ in Microsoft Word.
// Die Methode „StartTrackRevisions“ hat keinen Einfluss auf ihren Wert.
// und das Dokument verfolgt Revisionen programmgesteuert, obwohl es den Wert „false“ hat.
// Wenn wir dieses Dokument mit Microsoft Word öffnen, werden Revisionen nicht nachverfolgt.
Assert.IsFalse(doc.TrackRevisions);

// Wir haben mit dem Document Builder Text hinzugefügt, daher ist die erste Revision eine Revision vom Einfügungstyp.
Revision revision = doc.Revisions[0];
Assert.AreEqual("John Doe", revision.Author);
Assert.AreEqual("This is revision #1. ", revision.ParentNode.GetText());
Assert.AreEqual(RevisionType.Insertion, revision.RevisionType);
Assert.AreEqual(revision.DateTime.Date, DateTime.Now.Date);
Assert.AreEqual(doc.Revisions.Groups[0], revision.Group);

// Einen Lauf entfernen, um eine Revision vom Löschtyp zu erstellen.
doc.FirstSection.Body.FirstParagraph.Runs[0].Remove();

// Durch das Hinzufügen einer neuen Revision wird diese am Anfang der Revisionssammlung platziert.
Assert.AreEqual(RevisionType.Deletion, doc.Revisions[0].RevisionType);
Assert.AreEqual(2, doc.Revisions.Count);

// Einfügungsrevisionen werden im Dokumenttext angezeigt, noch bevor wir die Revision akzeptieren/ablehnen.
// Durch das Ablehnen der Revision werden ihre Knoten aus dem Hauptteil entfernt. Umgekehrt löschen Knoten, aus denen sie besteht, Revisionen
// bleiben auch im Dokument, bis wir die Überarbeitung akzeptieren.
Assert.AreEqual("This does not count as a revision. This is revision #1.", doc.GetText().Trim());

// Durch Akzeptieren der Löschrevision wird der übergeordnete Knoten aus dem Absatztext entfernt
// und dann die Revision der Sammlung selbst entfernen.
doc.Revisions[0].Accept();

Assert.AreEqual(1, doc.Revisions.Count);
Assert.AreEqual("This is revision #1.", doc.GetText().Trim());

builder.Writeln("");
builder.Write("This is revision #2.");

// Verschieben Sie nun den Knoten, um einen beweglichen Revisionstyp zu erstellen.
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

// Die verschobene Revision befindet sich jetzt an Index 1. Lehnen Sie die Revision ab, um ihren Inhalt zu verwerfen.
doc.Revisions[1].Reject();

Assert.AreEqual(6, doc.Revisions.Count);
Assert.AreEqual("This is revision #1. \rThis is revision #2.", doc.GetText().Trim());
```

### Siehe auch

* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)


