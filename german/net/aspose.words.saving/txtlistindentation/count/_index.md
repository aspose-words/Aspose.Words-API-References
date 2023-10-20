---
title: TxtListIndentation.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words für .NET
description: TxtListIndentation Count eigendom. Ruft ab oder legt fest wie vieleCharacter als Einrückung pro Listenebene zu verwenden. Der Standardwert ist 0 das bedeutet keine Einrückung in C#.
type: docs
weight: 30
url: /de/net/aspose.words.saving/txtlistindentation/count/
---
## TxtListIndentation.Count property

Ruft ab oder legt fest, wie viele[`Character`](../character/) als Einrückung pro Listenebene zu verwenden. Der Standardwert ist 0, das bedeutet keine Einrückung.

```csharp
public int Count { get; set; }
```

## Beispiele

Zeigt, wie die Listeneinrückung beim Speichern eines Dokuments im Klartext konfiguriert wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Erstellen Sie eine Liste mit drei Einrückungsebenen.
builder.ListFormat.ApplyNumberDefault();
builder.Writeln("Item 1");
builder.ListFormat.ListIndent();
builder.Writeln("Item 2");
builder.ListFormat.ListIndent(); 
builder.Write("Item 3");

// Erstelle ein „TxtSaveOptions“-Objekt, das wir an die „Save“-Methode des Dokuments übergeben können
// um zu ändern, wie wir das Dokument im Klartext speichern.
TxtSaveOptions txtSaveOptions = new TxtSaveOptions();

// Legen Sie die Eigenschaft „Character“ fest, um ein zu verwendendes Zeichen zuzuweisen
// zum Auffüllen, das die Einrückung von Listen im Klartext simuliert.
txtSaveOptions.ListIndentation.Character = ' ';

// Legen Sie die Eigenschaft „Count“ fest, um die Häufigkeit anzugeben
// um das Füllzeichen für jede Listeneinrückungsebene zu platzieren.
txtSaveOptions.ListIndentation.Count = 3;

doc.Save(ArtifactsDir + "TxtSaveOptions.TxtListIndentation.txt", txtSaveOptions);

string docText = File.ReadAllText(ArtifactsDir + "TxtSaveOptions.TxtListIndentation.txt");

Assert.AreEqual("1. Item 1\r\n" +
                "   a. Item 2\r\n" +
                "      i. Item 3\r\n", docText);
```

### Siehe auch

* class [TxtListIndentation](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
