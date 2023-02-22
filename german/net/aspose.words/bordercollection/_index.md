---
title: Class BorderCollection
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.BorderCollection klas. Eine Sammlung von BorderObjekten.
type: docs
weight: 80
url: /de/net/aspose.words/bordercollection/
---
## BorderCollection class

Eine Sammlung von Border-Objekten.

```csharp
public sealed class BorderCollection : IEnumerable<Border>
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Bottom](../../aspose.words/bordercollection/bottom/) { get; } | Ruft den unteren Rand ab. |
| [Color](../../aspose.words/bordercollection/color/) { get; set; } | Ruft die Rahmenfarbe ab oder legt sie fest. |
| [Count](../../aspose.words/bordercollection/count/) { get; } | Ruft die Anzahl der Rahmen in der Sammlung ab. |
| [DistanceFromText](../../aspose.words/bordercollection/distancefromtext/) { get; set; } | Ermittelt oder setzt den Abstand des Randes vom Text in Punkten. |
| [Horizontal](../../aspose.words/bordercollection/horizontal/) { get; } | Ruft den horizontalen Rahmen ab, der zwischen Zellen oder übereinstimmenden Absätzen verwendet wird. |
| [Item](../../aspose.words/bordercollection/item/) { get; } | Ruft ein Rahmenobjekt nach Rahmentyp ab. (2 indexers) |
| [Left](../../aspose.words/bordercollection/left/) { get; } | Ruft den linken Rand ab. |
| [LineStyle](../../aspose.words/bordercollection/linestyle/) { get; set; } | Ruft den Rahmenstil ab oder legt ihn fest. |
| [LineWidth](../../aspose.words/bordercollection/linewidth/) { get; set; } | Liest oder setzt die Rahmenbreite in Punkt. |
| [Right](../../aspose.words/bordercollection/right/) { get; } | Ruft den rechten Rand ab. |
| [Shadow](../../aspose.words/bordercollection/shadow/) { get; set; } | Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob der Rahmen einen Schatten hat. |
| [Top](../../aspose.words/bordercollection/top/) { get; } | Ruft den oberen Rand ab. |
| [Vertical](../../aspose.words/bordercollection/vertical/) { get; } | Ruft den vertikalen Rahmen ab, der zwischen Zellen verwendet wird. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [ClearFormatting](../../aspose.words/bordercollection/clearformatting/)() | Entfernt alle Ränder eines Objekts. |
| [Equals](../../aspose.words/bordercollection/equals/#equals)(BorderCollection) | Vergleicht Sammlungen von Grenzen. |
| [GetEnumerator](../../aspose.words/bordercollection/getenumerator/)() | Gibt ein Aufzählungsobjekt zurück, das verwendet werden kann, um über alle Grenzen in der Sammlung zu iterieren. |

### Bemerkungen

Unterschiedliche Dokumentelemente haben unterschiedliche Ränder. Zum Beispiel hat ParagraphFormat einen unteren, linken, rechten und oberen Rand. Sie können für jeden Rand unabhängig voneinander unterschiedliche Formatierungen festlegen oder alle Ränder aufzählen und dieselbe Formatierung anwenden.

### Beispiele

Zeigt, wie Sie einen Absatz mit einem oberen Rand einfügen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Border topBorder = builder.ParagraphFormat.Borders[BorderType.Top];
topBorder.Color = Color.Red;
topBorder.LineWidth = 4.0d;
topBorder.LineStyle = LineStyle.DashSmallGap;

builder.Writeln("Text with a red top border.");

doc.Save(ArtifactsDir + "Border.ParagraphTopBorder.docx");
```

### Siehe auch

* class [Border](../border/)
* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)


