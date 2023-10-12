---
title: TxtListIndentation.Character
second_title: Aspose.Words für .NET-API-Referenz
description: TxtListIndentation eigendom. Ruft ab oder legt fest welches Zeichen zum Einrücken von Listenebenen verwendet werden soll. Der Standardwert ist 0 das heißt es gibt keine Einrückung.
type: docs
weight: 20
url: /de/net/aspose.words.saving/txtlistindentation/character/
---
## TxtListIndentation.Character property

Ruft ab oder legt fest, welches Zeichen zum Einrücken von Listenebenen verwendet werden soll. Der Standardwert ist „\0“, das heißt, es gibt keine Einrückung.

```csharp
public char Character { get; set; }
```

### Beispiele

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
* namensraum [Aspose.Words.Saving](../../txtlistindentation/)
* Montage [Aspose.Words](../../../)


