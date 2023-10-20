---
title: NodeCollection.Insert
linktitle: Insert
articleTitle: Insert
second_title: Aspose.Words für .NET
description: NodeCollection Insert methode. Fügt am angegebenen Index einen Knoten in die Sammlung ein in C#.
type: docs
weight: 80
url: /de/net/aspose.words/nodecollection/insert/
---
## NodeCollection.Insert method

Fügt am angegebenen Index einen Knoten in die Sammlung ein.

```csharp
public void Insert(int index, Node node)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| index | Int32 | Der nullbasierte Index des Knotens. Negative Indizes sind zulässig und zeigen den Zugriff vom Ende der Liste an. Beispielsweise bedeutet -1 den letzten Knoten, -2 den vorletzten und so weiter. |
| node | Node | Der einzufügende Knoten. |

### Ausnahmen

| Ausnahme | Bedingung |
| --- | --- |
| NotSupportedException | Der[`NodeCollection`](../) ist eine „tiefe“ Sammlung. |

## Bemerkungen

Der Knoten wird als untergeordnetes Element in das Knotenobjekt eingefügt, aus dem die Sammlung erstellt wurde.

Wenn der Index gleich oder größer ist[`Count`](../count/), wird der Knoten am Ende der Sammlung hinzugefügt.

Wenn der Index negativ ist und sein absoluter Wert größer ist als[`Count`](../count/), wird der Knoten am Ende der Sammlung hinzugefügt.

Wenn der einzufügende Knoten aus einem anderen Dokument erstellt wurde, sollten Sie verwenden.[`ImportNode`](../../documentbase/importnode/) um den Knoten in das aktuelle Dokument zu importieren. Der importierte Knoten kann dann in das aktuelle Dokument eingefügt werden.

## Beispiele

Zeigt, wie mit einer NodeCollection gearbeitet wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fügen Sie dem Dokument Text hinzu, indem Sie Runs mit einem DocumentBuilder einfügen.
builder.Write("Run 1. ");
builder.Write("Run 2. ");

// Jeder Aufruf der Methode „Write“ erstellt einen neuen Run,
// die dann in der RunCollection des übergeordneten Absatzes erscheint.
RunCollection runs = doc.FirstSection.Body.FirstParagraph.Runs;

Assert.AreEqual(2, runs.Count);

// Wir können einen Knoten auch manuell in die RunCollection einfügen.
Run newRun = new Run(doc, "Run 3. ");
runs.Insert(3, newRun);

Assert.True(runs.Contains(newRun));
Assert.AreEqual("Run 1. Run 2. Run 3.", doc.GetText().Trim());

// Auf einzelne Läufe zugreifen und sie entfernen, um ihren Text aus dem Dokument zu entfernen.
Run run = runs[1];
runs.Remove(run);

Assert.AreEqual("Run 1. Run 3.", doc.GetText().Trim());
Assert.NotNull(run);
Assert.False(runs.Contains(run));
```

### Siehe auch

* class [Node](../../node/)
* class [NodeCollection](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
