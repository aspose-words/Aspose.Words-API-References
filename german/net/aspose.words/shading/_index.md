---
title: Class Shading
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Shading klas. Enthält Schattierungsattribute für ein Objekt.
type: docs
weight: 5990
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
| [BackgroundPatternColor](../../aspose.words/shading/backgroundpatterncolor/) { get; set; } | Ruft die Farbe ab, die auf den Hintergrund des angewendet wird, oder legt diese fest`Shading` Objekt. |
| [BackgroundPatternThemeColor](../../aspose.words/shading/backgroundpatternthemecolor/) { get; set; } | Ruft die Designfarbe des Hintergrundmusters in dem damit verbundenen angewendeten Farbschema ab oder legt diese fest`Shading` Objekt. |
| [BackgroundTintAndShade](../../aspose.words/shading/backgroundtintandshade/) { get; set; } | Ruft einen Double-Wert ab oder legt diesen fest, der die Hintergrundfarbe eines Themas aufhellt oder abdunkelt. |
| [ForegroundPatternColor](../../aspose.words/shading/foregroundpatterncolor/) { get; set; } | Ruft die Farbe ab, die auf den Vordergrund des angewendet wird, oder legt diese fest`Shading` Objekt. |
| [ForegroundPatternThemeColor](../../aspose.words/shading/foregroundpatternthemecolor/) { get; set; } | Ruft die Vordergrundmuster-Designfarbe im angewendeten Farbschema ab, das diesem zugeordnet ist, oder legt diese fest`Shading` Objekt. |
| [ForegroundTintAndShade](../../aspose.words/shading/foregroundtintandshade/) { get; set; } | Ruft einen Double-Wert ab oder legt ihn fest, der eine Vordergrund-Themenfarbe heller oder dunkler macht. |
| [Texture](../../aspose.words/shading/texture/) { get; set; } | Ruft die Schattierungstextur ab oder legt sie fest. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [ClearFormatting](../../aspose.words/shading/clearformatting/)() | Entfernt die Schattierung vom Objekt. |
| override [Equals](../../aspose.words/shading/equals/#equals_1)(object) | Bestimmt, ob das angegebene Objekt den gleichen Wert wie das aktuelle Objekt hat. |
| [Equals](../../aspose.words/shading/equals/#equals)(Shading) | Bestimmt, ob die angegebene`Shading` ist vom Wert her gleich dem Strom`Shading` . |
| override [GetHashCode](../../aspose.words/shading/gethashcode/)() | Dient als Hash-Funktion für diesen Typ. |

### Beispiele

Zeigt, wie Text mit Rändern und Schattierungen dekoriert wird.

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

Zeigt, wie Sie beim Erstellen einer Tabelle Rahmen- und Schattierungsfarben anwenden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Eine Tabelle starten und eine Standardfarbe/-stärke für ihre Ränder festlegen.
Table table = builder.StartTable();
table.SetBorders(LineStyle.Single, 2.0, Color.Black);

// Erstelle eine Zeile mit zwei Zellen mit unterschiedlichen Hintergrundfarben.
builder.InsertCell();
builder.CellFormat.Shading.BackgroundPatternColor = Color.LightSkyBlue;
builder.Writeln("Row 1, Cell 1.");
builder.InsertCell();
builder.CellFormat.Shading.BackgroundPatternColor = Color.Orange;
builder.Writeln("Row 1, Cell 2.");
builder.EndRow();

// Zellenformatierung zurücksetzen, um die Hintergrundfarben zu deaktivieren
// Legen Sie eine benutzerdefinierte Rahmenstärke für alle neuen Zellen fest, die vom Builder erstellt wurden.
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


