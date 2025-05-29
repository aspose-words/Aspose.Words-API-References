---
title: ConditionalStyle Class
linktitle: ConditionalStyle
articleTitle: ConditionalStyle
second_title: Aspose.Words für .NET
description: Entdecken Sie die Aspose.Words.ConditionalStyle-Klasse für erweiterte Tabellenformatierung. Optimieren Sie Ihre Dokumente mit dynamischen Stilen und verbessern Sie mühelos die Lesbarkeit.
type: docs
weight: 510
url: /de/net/aspose.words/conditionalstyle/
---
## ConditionalStyle class

Stellt eine spezielle Formatierung dar, die auf einen Bereich einer Tabelle mit zugewiesenem Tabellenstil angewendet wird.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Tabellen](https://docs.aspose.com/words/net/working-with-tables/) Dokumentationsartikel.

```csharp
public sealed class ConditionalStyle
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Borders](../../aspose.words/conditionalstyle/borders/) { get; } | Ruft die Sammlung der Standardzellenränder für den bedingten Stil ab. |
| [BottomPadding](../../aspose.words/conditionalstyle/bottompadding/) { get; set; } | Ruft den Abstand (in Punkten) ab, der unterhalb des Inhalts von Tabellenzellen hinzugefügt werden soll, oder legt diesen fest. |
| [Font](../../aspose.words/conditionalstyle/font/) { get; } | Ruft die Zeichenformatierung des bedingten Stils ab. |
| [LeftPadding](../../aspose.words/conditionalstyle/leftpadding/) { get; set; } | Ruft den Abstand (in Punkten) ab, der links vom Inhalt der Tabellenzellen hinzugefügt werden soll, oder legt diesen fest. |
| [ParagraphFormat](../../aspose.words/conditionalstyle/paragraphformat/) { get; } | Ruft die Absatzformatierung des bedingten Stils ab. |
| [RightPadding](../../aspose.words/conditionalstyle/rightpadding/) { get; set; } | Ruft den Abstand (in Punkten) ab, der rechts vom Inhalt der Tabellenzellen hinzugefügt werden soll, oder legt diesen fest. |
| [Shading](../../aspose.words/conditionalstyle/shading/) { get; } | Erhält eine[`Shading`](../shading/) Objekt, das sich auf die Schattierungsformatierung für diesen bedingten Stil bezieht. |
| [TopPadding](../../aspose.words/conditionalstyle/toppadding/) { get; set; } | Ruft den Abstand (in Punkten) ab, der über dem Inhalt der Tabellenzellen hinzugefügt werden soll, oder legt diesen fest. |
| [Type](../../aspose.words/conditionalstyle/type/) { get; } | Ruft den Tabellenbereich ab, auf den sich dieser bedingte Stil bezieht. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [ClearFormatting](../../aspose.words/conditionalstyle/clearformatting/)() | Löscht die Formatierung dieses bedingten Stils. |
| override [Equals](../../aspose.words/conditionalstyle/equals/)(*object*) | Vergleicht diesen bedingten Stil mit dem angegebenen Objekt. |
| override [GetHashCode](../../aspose.words/conditionalstyle/gethashcode/)() | Berechnet den Hashcode für dieses Objekt. |

## Beispiele

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

// Erstellen Sie einen benutzerdefinierten Tabellenstil.
TableStyle tableStyle = (TableStyle)doc.Styles.Add(StyleType.Table, "MyTableStyle1");

// Bedingte Stile sind Formatierungsänderungen, die nur einige Zellen der Tabelle betreffen
// basierend auf einem Prädikat, z. B. dass sich die Zellen in der letzten Zeile befinden.
// Unten sind drei Möglichkeiten aufgeführt, um auf die bedingten Stile eines Tabellenstils aus der Sammlung „ConditionalStyles“ zuzugreifen.
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

// Den benutzerdefinierten Stil, der alle bedingten Stile enthält, auf die Tabelle anwenden.
table.Style = tableStyle;

// Unser Stil wendet standardmäßig einige bedingte Stile an.
Assert.AreEqual(TableStyleOptions.FirstRow | TableStyleOptions.FirstColumn | TableStyleOptions.RowBands, 
    table.StyleOptions);

// Alle anderen Stile müssen wir selbst über die Eigenschaft „StyleOptions“ aktivieren.
table.StyleOptions = table.StyleOptions | TableStyleOptions.LastRow | TableStyleOptions.LastColumn;

doc.Save(ArtifactsDir + "Table.ConditionalStyles.docx");
```

### Siehe auch

* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)
