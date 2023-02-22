---
title: Class ConditionalStyle
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.ConditionalStyle klas. Stellt eine spezielle Formatierung dar die auf einen Bereich einer Tabelle mit zugewiesenem Tabellenstil angewendet wird.
type: docs
weight: 300
url: /de/net/aspose.words/conditionalstyle/
---
## ConditionalStyle class

Stellt eine spezielle Formatierung dar, die auf einen Bereich einer Tabelle mit zugewiesenem Tabellenstil angewendet wird.

```csharp
public sealed class ConditionalStyle
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Borders](../../aspose.words/conditionalstyle/borders/) { get; } | Ruft die Sammlung von Standardzellenrahmen für den bedingten Stil ab. |
| [BottomPadding](../../aspose.words/conditionalstyle/bottompadding/) { get; set; } | Ruft den Abstand (in Punkt) ab oder legt ihn fest, der unter dem Inhalt von Tabellenzellen hinzugefügt werden soll. |
| [Font](../../aspose.words/conditionalstyle/font/) { get; } | Ruft die Zeichenformatierung des bedingten Stils ab. |
| [LeftPadding](../../aspose.words/conditionalstyle/leftpadding/) { get; set; } | Ruft den Platz (in Punkten) ab oder legt ihn fest, der links vom Inhalt der Tabellenzellen hinzugefügt werden soll. |
| [ParagraphFormat](../../aspose.words/conditionalstyle/paragraphformat/) { get; } | Ruft die Absatzformatierung des bedingten Stils ab. |
| [RightPadding](../../aspose.words/conditionalstyle/rightpadding/) { get; set; } | Ruft den Abstand (in Punkten) ab oder legt ihn fest, der rechts vom Inhalt der Tabellenzellen hinzugefügt werden soll. |
| [Shading](../../aspose.words/conditionalstyle/shading/) { get; } | erhält a[`Shading`](../shading/) Objekt, das sich auf die Schattierungsformatierung für diesen bedingten Stil bezieht. |
| [TopPadding](../../aspose.words/conditionalstyle/toppadding/) { get; set; } | Ruft den Abstand (in Punkten) ab oder legt ihn fest, der über dem Inhalt von Tabellenzellen hinzugefügt werden soll. |
| [Type](../../aspose.words/conditionalstyle/type/) { get; } | Ruft den Tabellenbereich ab, auf den sich dieser bedingte Stil bezieht. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [ClearFormatting](../../aspose.words/conditionalstyle/clearformatting/)() | Löscht die Formatierung dieses bedingten Stils. |
| override [Equals](../../aspose.words/conditionalstyle/equals/)(object) |  |
| override [GetHashCode](../../aspose.words/conditionalstyle/gethashcode/)() | Berechnet Hashcode für dieses Objekt. |

### Beispiele

Zeigt, wie mit bestimmten Bereichsstilen einer Tabelle gearbeitet wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Cell 1");
builder.InsertCell();
builder.Write("Cell 2");
builder.EndRow();
builder.InsertCell();
builder.Write("Cell 3");
builder.InsertCell();
builder.Write("Cell 4");
builder.EndTable();

// Einen benutzerdefinierten Tabellenstil erstellen.
TableStyle tableStyle = (TableStyle)doc.Styles.Add(StyleType.Table, "MyTableStyle1");

// Bedingte Stile sind Formatierungsänderungen, die nur einige Zellen der Tabelle betreffen
// basierend auf einem Prädikat, z. B. die Zellen in der letzten Zeile.
// Im Folgenden finden Sie drei Möglichkeiten, auf die bedingten Stile eines Tabellenstils aus der Sammlung "ConditionalStyles" zuzugreifen.
// 1 - Nach Stiltyp:
tableStyle.ConditionalStyles[ConditionalStyleType.FirstRow].Shading.BackgroundPatternColor = Color.AliceBlue;

// 2 - Nach Index:
tableStyle.ConditionalStyles[0].Borders.Color = Color.Black;
tableStyle.ConditionalStyles[0].Borders.LineStyle = LineStyle.DotDash;
Assert.AreEqual(ConditionalStyleType.FirstRow, tableStyle.ConditionalStyles[0].Type);

// 3 - Als Eigenschaft:
tableStyle.ConditionalStyles.FirstRow.ParagraphFormat.Alignment = ParagraphAlignment.Center;

// Auffüllung und Textformatierung auf bedingte Stile anwenden.
tableStyle.ConditionalStyles.LastRow.BottomPadding = 10;
tableStyle.ConditionalStyles.LastRow.LeftPadding = 10;
tableStyle.ConditionalStyles.LastRow.RightPadding = 10;
tableStyle.ConditionalStyles.LastRow.TopPadding = 10;
tableStyle.ConditionalStyles.LastColumn.Font.Bold = true;

// Alle möglichen Stilbedingungen auflisten.
using (IEnumerator<ConditionalStyle> enumerator = tableStyle.ConditionalStyles.GetEnumerator())
{
    while (enumerator.MoveNext())
    {
        ConditionalStyle currentStyle = enumerator.Current;
        if (currentStyle != null) Console.WriteLine(currentStyle.Type);
    }
}

// Anwenden des benutzerdefinierten Stils, der alle bedingten Stile enthält, auf die Tabelle.
table.Style = tableStyle;

// Unser Stil wendet standardmäßig einige bedingte Stile an.
Assert.AreEqual(TableStyleOptions.FirstRow | TableStyleOptions.FirstColumn | TableStyleOptions.RowBands, 
    table.StyleOptions);

// Wir müssen alle anderen Stile selbst über die Eigenschaft "StyleOptions" aktivieren.
table.StyleOptions = table.StyleOptions | TableStyleOptions.LastRow | TableStyleOptions.LastColumn;

doc.Save(ArtifactsDir + "Table.ConditionalStyles.docx");
```

### Siehe auch

* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)


