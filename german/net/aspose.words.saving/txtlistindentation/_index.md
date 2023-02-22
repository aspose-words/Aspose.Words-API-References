---
title: Class TxtListIndentation
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Saving.TxtListIndentation klas. Gibt an wie Listenebenen eingerückt werden wenn das Dokument exportiert wirdText format.
type: docs
weight: 5370
url: /de/net/aspose.words.saving/txtlistindentation/
---
## TxtListIndentation class

Gibt an, wie Listenebenen eingerückt werden, wenn das Dokument exportiert wirdText format.

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
| [Character](../../aspose.words.saving/txtlistindentation/character/) { get; set; } | Ruft ab oder legt fest, welches Zeichen zum Einrücken von Listenebenen verwendet werden soll. Der Standardwert ist '\0', das heißt, es gibt keinen Einzug. |
| [Count](../../aspose.words.saving/txtlistindentation/count/) { get; set; } | Ruft ab oder setzt wie viele[`Character`](./character/) als Einrückung pro Listenebene zu verwenden. Der Standardwert ist 0, dh keine Einrückung. |

### Beispiele

Zeigt, wie der Listeneinzug beim Speichern eines Dokuments im Klartext konfiguriert wird.

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

// Erstellen Sie ein "TxtSaveOptions"-Objekt, das wir an die "Save"-Methode des Dokuments übergeben können
// um zu ändern, wie wir das Dokument im Klartext speichern.
TxtSaveOptions txtSaveOptions = new TxtSaveOptions();

// Legen Sie die "Character"-Eigenschaft fest, um ein zu verwendendes Zeichen zuzuweisen
// für Padding, das Listeneinrückung im Klartext simuliert.
txtSaveOptions.ListIndentation.Character = ' ';

// Legen Sie die Eigenschaft "Count" fest, um die Anzahl der Male anzugeben
// zum Platzieren des Füllzeichens für jede Einrückungsebene der Liste.
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


