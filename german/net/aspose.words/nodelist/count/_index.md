---
title: NodeList.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words für .NET
description: Entdecken Sie die NodeList Count-Eigenschaft, um einfach die Gesamtzahl der Knoten in Ihrer Liste abzurufen und so die Effizienz Ihrer Webentwicklung zu steigern.
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

* class [NodeList](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
