---
title: NodeCollection.Remove
linktitle: Remove
articleTitle: Remove
second_title: Aspose.Words für .NET
description: Entfernen Sie mühelos Knoten aus Ihrem Dokument mit der Methode „NodeCollection Remove“, wodurch Ihre Datenverwaltung optimiert und die Leistung verbessert wird.
type: docs
weight: 90
url: /de/net/aspose.words/nodecollection/remove/
---
## NodeCollection.Remove method

Entfernt den Knoten aus der Sammlung und aus dem Dokument.

```csharp
public void Remove(Node node)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| node | Node | Der zu entfernende Knoten. |

## Beispiele

Zeigt, wie mit einer NodeCollection gearbeitet wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fügen Sie dem Dokument Text hinzu, indem Sie mithilfe eines DocumentBuilder Runs einfügen.
builder.Write("Run 1. ");
builder.Write("Run 2. ");

// Jeder Aufruf der Methode "Write" erzeugt einen neuen Run,
// die dann in der RunCollection des übergeordneten Absatzes erscheint.
RunCollection runs = doc.FirstSection.Body.FirstParagraph.Runs;

Assert.AreEqual(2, runs.Count);

// Wir können auch manuell einen Knoten in die RunCollection einfügen.
Run newRun = new Run(doc, "Run 3. ");
runs.Insert(3, newRun);

Assert.True(runs.Contains(newRun));
Assert.AreEqual("Run 1. Run 2. Run 3.", doc.GetText().Trim());

// Greifen Sie auf einzelne Läufe zu und entfernen Sie sie, um ihren Text aus dem Dokument zu entfernen.
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
