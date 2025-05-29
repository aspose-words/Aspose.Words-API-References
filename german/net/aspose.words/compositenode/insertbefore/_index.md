---
title: CompositeNode.InsertBefore
linktitle: InsertBefore
articleTitle: InsertBefore
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie Sie mit der CompositeNode-Methode „InsertBefore“ Knoten nahtlos vor Referenzknoten einfügen und so Ihre Datenstrukturverwaltung verbessern.
type: docs
weight: 160
url: /de/net/aspose.words/compositenode/insertbefore/
---
## CompositeNode.InsertBefore&lt;T&gt; method

Fügt den angegebenen Knoten unmittelbar vor dem angegebenen Referenzknoten ein.

```csharp
public T InsertBefore<T>(T newChild, Node refChild)
    where T : Node
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| newChild | T | Der[`Node`](../../node/) einfügen. |
| refChild | Node | Der[`Node`](../../node/) das ist der Referenzknoten. Der*newChild* wird vor diesem Knoten platziert. |

### Rückgabewert

Der eingefügte Knoten.

## Bemerkungen

Wenn*refChild* Ist`null` , Einsätze*newChild* am Ende der Liste der untergeordneten Knoten.

Wenn die*newChild* ist bereits im Baum vorhanden, wird es zunächst entfernt.

Wenn der einzufügende Knoten aus einem anderen Dokument erstellt wurde, sollten Sie verwenden.[`ImportNode`](../../documentbase/importnode/) um den Knoten in das aktuelle Dokument zu importieren. Der importierte Knoten kann dann in das aktuelle Dokument eingefügt werden.

## Beispiele

Zeigt, wie untergeordnete Knoten in der Sammlung untergeordneter Knoten eines CompositeNode hinzugefügt, aktualisiert und gelöscht werden.

```csharp
Document doc = new Document();

// Ein leeres Dokument hat standardmäßig einen Absatz.
Assert.AreEqual(1, doc.FirstSection.Body.Paragraphs.Count);

// Zusammengesetzte Knoten wie unser Absatz können andere zusammengesetzte und Inline-Knoten als untergeordnete Elemente enthalten.
Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;
Run paragraphText = new Run(doc, "Initial text. ");
paragraph.AppendChild(paragraphText);

// Erstellen Sie drei weitere Run-Knoten.
Run run1 = new Run(doc, "Run 1. ");
Run run2 = new Run(doc, "Run 2. ");
Run run3 = new Run(doc, "Run 3. ");

// Der Dokumenttext zeigt diese Läufe erst an, wenn wir sie in einen zusammengesetzten Knoten einfügen
// das selbst ein Teil des Knotenbaums des Dokuments ist, wie wir es beim ersten Durchlauf getan haben.
// Wir können bestimmen, wo der Textinhalt der Knoten, die wir einfügen
// erscheint im Dokument, indem eine Einfügeposition relativ zu einem anderen Knoten im Absatz angegeben wird.
Assert.AreEqual("Initial text.", paragraph.GetText().Trim());

// Fügen Sie den zweiten Lauf in den Absatz vor dem ersten Lauf ein.
paragraph.InsertBefore(run2, paragraphText);

Assert.AreEqual("Run 2. Initial text.", paragraph.GetText().Trim());

// Fügen Sie den dritten Lauf nach dem ersten Lauf ein.
paragraph.InsertAfter(run3, paragraphText);

Assert.AreEqual("Run 2. Initial text. Run 3.", paragraph.GetText().Trim());

// Fügen Sie den ersten Lauf am Anfang der untergeordneten Knotensammlung des Absatzes ein.
paragraph.PrependChild(run1);

Assert.AreEqual("Run 1. Run 2. Initial text. Run 3.", paragraph.GetText().Trim());
Assert.AreEqual(4, paragraph.GetChildNodes(NodeType.Any, true).Count);

// Wir können den Inhalt des Laufs ändern, indem wir vorhandene untergeordnete Knoten bearbeiten und löschen.
((Run)paragraph.GetChildNodes(NodeType.Run, true)[1]).Text = "Updated run 2. ";
paragraph.GetChildNodes(NodeType.Run, true).Remove(paragraphText);

Assert.AreEqual("Run 1. Updated run 2. Run 3.", paragraph.GetText().Trim());
Assert.AreEqual(3, paragraph.GetChildNodes(NodeType.Any, true).Count);
```

### Siehe auch

* class [Node](../../node/)
* class [CompositeNode](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
