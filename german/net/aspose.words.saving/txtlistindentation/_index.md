---
title: TxtListIndentation Class
linktitle: TxtListIndentation
articleTitle: TxtListIndentation
second_title: Aspose.Words für .NET
description: Aspose.Words.Saving.TxtListIndentation klas. Gibt an wie Listenebenen eingerückt werden wenn das Dokument exportiert wirdText format in C#.
type: docs
weight: 5650
url: /de/net/aspose.words.saving/txtlistindentation/
---
## TxtListIndentation class

Gibt an, wie Listenebenen eingerückt werden, wenn das Dokument exportiert wirdText format.

Um mehr zu erfahren, besuchen Sie die[Speichern Sie ein Dokument](https://docs.aspose.com/words/net/save-a-document/) Dokumentationsartikel.

```csharp
public class TxtListIndentation
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [TxtListIndentation](txtlistindentation/)() | Default_Constructor |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Character](../../aspose.words.saving/txtlistindentation/character/) { get; set; } | Ruft ab oder legt fest, welches Zeichen zum Einrücken von Listenebenen verwendet werden soll. Der Standardwert ist „\0“, das heißt, es gibt keine Einrückung. |
| [Count](../../aspose.words.saving/txtlistindentation/count/) { get; set; } | Ruft ab oder legt fest, wie viele[`Character`](./character/) als Einrückung pro Listenebene zu verwenden. Der Standardwert ist 0, das bedeutet keine Einrückung. |

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

* namensraum [Aspose.Words.Saving](../../aspose.words.saving/)
* Montage [Aspose.Words](../../)
