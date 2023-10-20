---
title: NodeList.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words für .NET
description: NodeList Count eigendom. Ruft die Anzahl der Knoten in der Liste ab in C#.
type: docs
weight: 10
url: /de/net/aspose.words/nodelist/count/
---
## NodeList.Count property

Ruft die Anzahl der Knoten in der Liste ab.

```csharp
public int Count { get; }
```

## Beispiele

Zeigt, wie XPaths zum Navigieren in einer NodeList verwendet werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Einige Knoten mit einem DocumentBuilder einfügen.
builder.Writeln("Hello world!");

builder.StartTable();
builder.InsertCell();
builder.Write("Cell 1");
builder.InsertCell();
builder.Write("Cell 2");
builder.EndTable();

#if NET48 || JAVA
builder.InsertImage(Image.FromFile(ImageDir + "Logo.jpg"));
#elif NET5_0_OR_GREATER || __MOBILE__
using (SKBitmap image = SKBitmap.Decode(ImageDir + "Logo.jpg"))
    builder.InsertImage(image);
#endif

// Unser Dokument enthält drei Run-Knoten.
NodeList nodeList = doc.SelectNodes("//Laufen");

Assert.AreEqual(3, nodeList.Count);
Assert.True(nodeList.Any(n => n.GetText().Trim() == "Hello world!"));
Assert.True(nodeList.Any(n => n.GetText().Trim() == "Cell 1"));
Assert.True(nodeList.Any(n => n.GetText().Trim() == "Cell 2"));

// Verwenden Sie einen doppelten Schrägstrich, um alle Run-Knoten auszuwählen
// das sind indirekte Nachkommen eines Tabellenknotens, also die Läufe innerhalb der beiden von uns eingefügten Zellen.
nodeList = doc.SelectNodes("//Table//Laufen");

Assert.AreEqual(2, nodeList.Count);
Assert.True(nodeList.Any(n => n.GetText().Trim() == "Cell 1"));
Assert.True(nodeList.Any(n => n.GetText().Trim() == "Cell 2"));

// Einzelne Schrägstriche geben direkte Nachkommenbeziehungen an,
// was wir übersprungen haben, als wir doppelte Schrägstriche verwendet haben.
Assert.AreEqual(doc.SelectNodes(" //Tabelle//Ausführen"),
    doc.SelectNodes("//Tabelle/Zeile/Zelle/Absatz/Lauf"));

// Auf die Form zugreifen, die das von uns eingefügte Bild enthält.
nodeList = doc.SelectNodes("//Form");

Assert.AreEqual(1, nodeList.Count);

Shape shape = (Shape)nodeList[0];
Assert.True(shape.HasImage);
```

### Siehe auch

* class [NodeList](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
