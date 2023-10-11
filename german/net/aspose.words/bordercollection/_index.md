---
title: Class BorderCollection
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.BorderCollection klas. Eine Sammlung vonBorder Objekte.
type: docs
weight: 90
url: /de/net/aspose.words/bordercollection/
---
## BorderCollection class

Eine Sammlung von[`Border`](../border/) Objekte.

Um mehr zu erfahren, besuchen Sie die[Programmieren mit Dokumenten](https://docs.aspose.com/words/net/programming-with-documents/) Dokumentationsartikel.

```csharp
public sealed class BorderCollection : IEnumerable<Border>
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Bottom](../../aspose.words/bordercollection/bottom/) { get; } | Ruft den unteren Rand ab. |
| [Color](../../aspose.words/bordercollection/color/) { get; set; } | Ruft die Rahmenfarbe ab oder legt sie fest. |
| [Count](../../aspose.words/bordercollection/count/) { get; } | Ruft die Anzahl der Rahmen in der Sammlung ab. |
| [DistanceFromText](../../aspose.words/bordercollection/distancefromtext/) { get; set; } | Ermittelt oder legt den Abstand des Rahmens vom Text in Punkten fest. |
| [Horizontal](../../aspose.words/bordercollection/horizontal/) { get; } | Ruft den horizontalen Rahmen ab, der zwischen Zellen oder entsprechenden Absätzen verwendet wird. |
| [Item](../../aspose.words/bordercollection/item/) { get; } | Ruft a ab[`Border`](../border/) Objekt nach Rahmentyp. (2 indexers) |
| [Left](../../aspose.words/bordercollection/left/) { get; } | Ruft den linken Rand ab. |
| [LineStyle](../../aspose.words/bordercollection/linestyle/) { get; set; } | Ruft den Rahmenstil ab oder legt ihn fest. |
| [LineWidth](../../aspose.words/bordercollection/linewidth/) { get; set; } | Ruft die Rahmenbreite in Punkten ab oder legt sie fest. |
| [Right](../../aspose.words/bordercollection/right/) { get; } | Ermittelt den richtigen Rand. |
| [Shadow](../../aspose.words/bordercollection/shadow/) { get; set; } | Ruft einen Wert ab oder legt diesen fest, der angibt, ob der Rahmen einen Schatten hat. |
| [Top](../../aspose.words/bordercollection/top/) { get; } | Ruft den oberen Rand ab. |
| [Vertical](../../aspose.words/bordercollection/vertical/) { get; } | Ruft den vertikalen Rahmen ab, der zwischen Zellen verwendet wird. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [ClearFormatting](../../aspose.words/bordercollection/clearformatting/)() | Entfernt alle Ränder eines Objekts. |
| [Equals](../../aspose.words/bordercollection/equals/#equals)(BorderCollection) | Vergleicht Sammlungen von Rahmen. |
| [GetEnumerator](../../aspose.words/bordercollection/getenumerator/)() | Gibt ein Enumeratorobjekt zurück, das zum Durchlaufen aller Grenzen in der Sammlung verwendet werden kann. |

### Bemerkungen

Verschiedene Dokumentelemente haben unterschiedliche Ränder. Zum Beispiel:[`ParagraphFormat`](../paragraphformat/)hat[`Bottom`](./bottom/) ,[`Left`](./left/) ,[`Right`](./right/) Und[`Top`](./top/) borders. Sie können für jeden Rahmen unabhängig eine andere Formatierung festlegen oder alle Rahmen auflisten und dieselbe Formatierung anwenden.

### Beispiele

Zeigt, wie ein Absatz mit einem oberen Rand eingefügt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Border topBorder = builder.ParagraphFormat.Borders.Top;
topBorder.LineWidth = 4.0d;
topBorder.LineStyle = LineStyle.DashSmallGap;
// ThemeColor nur festlegen, wenn LineWidth oder LineStyle festgelegt ist.
topBorder.ThemeColor = ThemeColor.Accent1;
topBorder.TintAndShade = 0.25d;

builder.Writeln("Text with a top border.");

doc.Save(ArtifactsDir + "Border.ParagraphTopBorder.docx");
```

### Siehe auch

* class [Border](../border/)
* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)


