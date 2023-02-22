---
title: NodeList.Count
second_title: Aspose.Words für .NET-API-Referenz
description: NodeList eigendom. Ruft die Anzahl der Knoten in der Liste ab.
type: docs
weight: 10
url: /de/net/aspose.words/nodelist/count/
---
## NodeList.Count property

Ruft die Anzahl der Knoten in der Liste ab.

```csharp
public int Count { get; }
```

### Beispiele

Zeigt die Verwendung von XPaths zum Navigieren in einer NodeList.

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
// die indirekte Nachkommen eines Tabellenknotens sind, was die Läufe innerhalb der beiden von uns eingefügten Zellen wären.
nodeList = doc.SelectNodes("//Table//Laufen");

Assert.AreEqual(2, nodeList.Count);
Assert.True(nodeList.Any(n => n.GetText().Trim() == "Cell 1"));
Assert.True(nodeList.Any(n => n.GetText().Trim() == "Cell 2"));

// Einfache Schrägstriche geben direkte Nachkommenbeziehungen an,
// die wir übersprungen haben, als wir doppelte Schrägstriche verwendet haben.
Assert.AreEqual(doc.SelectNodes(" //Tabelle//Run"),
    doc.SelectNodes("//Tabelle/Zeile/Zelle/Absatz/Lauf"));

// Auf die Form zugreifen, die das eingefügte Bild enthält.
nodeList = doc.SelectNodes("//Form");

Assert.AreEqual(1, nodeList.Count);

Shape shape = (Shape)nodeList[0];
Assert.True(shape.HasImage);
```

### Siehe auch

* class [NodeList](../)
* namensraum [Aspose.Words](../../nodelist/)
* Montage [Aspose.Words](../../../)


