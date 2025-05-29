---
title: Shading Class
linktitle: Shading
articleTitle: Shading
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Shading, die Ihre Dokumente mit anpassbaren Schattierungsattributen für ein professionelles Aussehen aufwerten soll.
type: docs
weight: 6820
url: /de/net/aspose.words/shading/
---
## Shading class

Enthält Schattierungsattribute für ein Objekt.

Um mehr zu erfahren, besuchen Sie die[Programmieren mit Dokumenten](https://docs.aspose.com/words/net/programming-with-documents/) Dokumentationsartikel.

```csharp
public class Shading : InternableComplexAttr
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [BackgroundPatternColor](../../aspose.words/shading/backgroundpatterncolor/) { get; set; } | Ruft die Farbe ab oder legt sie fest, die auf den Hintergrund des`Shading` Objekt. |
| [BackgroundPatternThemeColor](../../aspose.words/shading/backgroundpatternthemecolor/) { get; set; } | Ruft die Hintergrundmuster-Designfarbe im angewendeten Farbschema ab oder legt sie fest, die mit diesem verknüpft ist.`Shading` Objekt. |
| [BackgroundTintAndShade](../../aspose.words/shading/backgroundtintandshade/) { get; set; } | Ruft einen Double-Wert ab oder legt ihn fest, der die Farbe eines Hintergrunddesigns aufhellt oder abdunkelt. |
| [ForegroundPatternColor](../../aspose.words/shading/foregroundpatterncolor/) { get; set; } | Ruft die Farbe ab oder legt sie fest, die auf den Vordergrund des`Shading` Objekt. |
| [ForegroundPatternThemeColor](../../aspose.words/shading/foregroundpatternthemecolor/) { get; set; } | Ruft die Vordergrundmuster-Designfarbe im angewendeten Farbschema ab oder legt sie fest, die mit diesem verknüpft ist.`Shading` Objekt. |
| [ForegroundTintAndShade](../../aspose.words/shading/foregroundtintandshade/) { get; set; } | Ruft einen Double-Wert ab oder legt ihn fest, der eine Vordergrunddesignfarbe aufhellt oder abdunkelt. |
| [Texture](../../aspose.words/shading/texture/) { get; set; } | Ruft die Schattierungstextur ab oder legt sie fest. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [ClearFormatting](../../aspose.words/shading/clearformatting/)() | Entfernt die Schattierung vom Objekt. |
| override [Equals](../../aspose.words/shading/equals/#equals_1)(*object*) | Bestimmt, ob das angegebene Objekt den gleichen Wert wie das aktuelle Objekt hat. |
| [Equals](../../aspose.words/shading/equals/#equals)(*Shading*) | Bestimmt, ob die angegebene`Shading` ist im Wert gleich dem aktuellen`Shading` . |
| override [GetHashCode](../../aspose.words/shading/gethashcode/)() | Dient als Hash-Funktion für diesen Typ. |

## Beispiele

Zeigt, wie Sie Text mit Rahmen und Schattierungen verzieren.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

BorderCollection borders = builder.ParagraphFormat.Borders;
borders.DistanceFromText = 20;
borders[BorderType.Left].LineStyle = LineStyle.Double;
borders[BorderType.Right].LineStyle = LineStyle.Double;
borders[BorderType.Top].LineStyle = LineStyle.Double;
borders[BorderType.Bottom].LineStyle = LineStyle.Double;

Shading shading = builder.ParagraphFormat.Shading;
shading.Texture = TextureIndex.TextureDiagonalCross;
shading.BackgroundPatternColor = Color.LightCoral;
shading.ForegroundPatternColor = Color.LightSalmon;

builder.Write("This paragraph is formatted with a double border and shading.");
doc.Save(ArtifactsDir + "DocumentBuilder.ApplyBordersAndShading.docx");
```

Zeigt, wie beim Erstellen einer Tabelle Rahmen- und Schattierungsfarben angewendet werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Starten Sie eine Tabelle und legen Sie eine Standardfarbe/-dicke für ihre Ränder fest.
Table table = builder.StartTable();
table.SetBorders(LineStyle.Single, 2.0, Color.Black);

// Erstellen Sie eine Zeile mit zwei Zellen mit unterschiedlichen Hintergrundfarben.
builder.InsertCell();
builder.CellFormat.Shading.BackgroundPatternColor = Color.LightSkyBlue;
builder.Writeln("Row 1, Cell 1.");
builder.InsertCell();
builder.CellFormat.Shading.BackgroundPatternColor = Color.Orange;
builder.Writeln("Row 1, Cell 2.");
builder.EndRow();

// Setzen Sie die Zellenformatierung zurück, um die Hintergrundfarben zu deaktivieren
// Legen Sie eine benutzerdefinierte Rahmenstärke für alle neuen Zellen fest, die vom Builder erstellt werden.
// dann baue eine zweite Reihe.
builder.CellFormat.ClearFormatting();
builder.CellFormat.Borders.Left.LineWidth = 4.0;
builder.CellFormat.Borders.Right.LineWidth = 4.0;
builder.CellFormat.Borders.Top.LineWidth = 4.0;
builder.CellFormat.Borders.Bottom.LineWidth = 4.0;

builder.InsertCell();
builder.Writeln("Row 2, Cell 1.");
builder.InsertCell();
builder.Writeln("Row 2, Cell 2.");

doc.Save(ArtifactsDir + "DocumentBuilder.TableBordersAndShading.docx");
```

### Siehe auch

* class [InternableComplexAttr](../internablecomplexattr/)
* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)
