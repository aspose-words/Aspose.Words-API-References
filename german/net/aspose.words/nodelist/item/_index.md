---
title: NodeList.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words für .NET
description: Greifen Sie mit der NodeList-Elementeigenschaft mühelos auf bestimmte Knoten zu. Rufen Sie Knoten nach Index ab, um die Datenbearbeitung zu optimieren und die Codierung zu optimieren.
type: docs
weight: 20
url: /de/net/aspose.words/nodelist/item/
---
## NodeList indexer

Ruft einen Knoten am angegebenen Index ab.

```csharp
public Node this[int index] { get; }
```

| Parameter | Beschreibung |
| --- | --- |
| index | Ein Index in der Liste der Knoten. |

## Bemerkungen

Der Index ist nullbasiert.

Negative Indizes sind zulässig und zeigen den Zugriff vom Ende der Sammlung an. Beispielsweise bedeutet -1 das letzte Element, -2 das vorletzte und so weiter.

Wenn der Index größer oder gleich der Anzahl der Elemente in der Liste ist, wird eine Nullreferenz zurückgegeben.

Wenn der Index negativ ist und sein absoluter Wert größer als die Anzahl der Elemente in der Liste ist, wird eine Nullreferenz zurückgegeben.

## Beispiele

Zeigt, wie XPaths zum Navigieren in einer NodeList verwendet werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fügen Sie einige Knoten mit einem DocumentBuilder ein.
builder.Writeln("Hello world!");

builder.StartTable();
builder.InsertCell();
builder.Write("Cell 1");
builder.InsertCell();
builder.Write("Cell 2");
builder.EndTable();

builder.InsertImage(ImageDir + "Logo.jpg");

// Unser Dokument enthält drei Run-Knoten.
NodeList nodeList = doc.SelectNodes("//Laufen");

Assert.AreEqual(3, nodeList.Count);
Assert.True(nodeList.Any(n => n.GetText().Trim() == "Hello world!"));
Assert.True(nodeList.Any(n => n.GetText().Trim() == "Cell 1"));
Assert.True(nodeList.Any(n => n.GetText().Trim() == "Cell 2"));

// Verwenden Sie einen doppelten Schrägstrich, um alle Run-Knoten auszuwählen
// die indirekte Nachkommen eines Tabellenknotens sind, also die Läufe innerhalb der beiden von uns eingefügten Zellen.
nodeList = doc.SelectNodes("//Tabelle//Ausführen");

Assert.AreEqual(2, nodeList.Count);
Assert.True(nodeList.Any(n => n.GetText().Trim() == "Cell 1"));
Assert.True(nodeList.Any(n => n.GetText().Trim() == "Cell 2"));

// Einzelne Schrägstriche geben direkte Nachkommenbeziehungen an,
// die wir übersprungen haben, als wir doppelte Schrägstriche verwendet haben.
Assert.AreEqual(doc.SelectNodes("    //Tabelle//Ausführen"),
    doc.SelectNodes("//Tabelle/Zeile/Zelle/Absatz/Ausführen"));

// Greifen Sie auf die Form zu, die das von uns eingefügte Bild enthält.
nodeList = doc.SelectNodes("//Form");

Assert.AreEqual(1, nodeList.Count);

Shape shape = (Shape)nodeList[0];
Assert.True(shape.HasImage);
```

### Siehe auch

* class [Node](../../node/)
* class [NodeList](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
