---
title: ConditionalStyleCollection Class
linktitle: ConditionalStyleCollection
articleTitle: ConditionalStyleCollection
second_title: Aspose.Words für .NET
description: Erkunden Sie die Klasse Aspose.Words.ConditionalStyleCollection, um ConditionalStyle-Objekte effektiv zu verwalten und die Dokumentformatierung und -anpassung zu verbessern.
type: docs
weight: 520
url: /de/net/aspose.words/conditionalstylecollection/
---
## ConditionalStyleCollection class

Stellt eine Sammlung von[`ConditionalStyle`](../conditionalstyle/) Objekte.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Tabellen](https://docs.aspose.com/words/net/working-with-tables/) Dokumentationsartikel.

```csharp
public sealed class ConditionalStyleCollection : IEnumerable<ConditionalStyle>
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [BottomLeftCell](../../aspose.words/conditionalstylecollection/bottomleftcell/) { get; } | Ruft den Zellenstil unten links ab. |
| [BottomRightCell](../../aspose.words/conditionalstylecollection/bottomrightcell/) { get; } | Ruft den Zellenstil unten rechts ab. |
| [Count](../../aspose.words/conditionalstylecollection/count/) { get; } | Ruft die Anzahl der bedingten Stile in der Sammlung ab. |
| [EvenColumnBanding](../../aspose.words/conditionalstylecollection/evencolumnbanding/) { get; } | Ruft den gleichmäßigen Spaltenbandstil ab. |
| [EvenRowBanding](../../aspose.words/conditionalstylecollection/evenrowbanding/) { get; } | Ruft den geraden Zeilenbandstil ab. |
| [FirstColumn](../../aspose.words/conditionalstylecollection/firstcolumn/) { get; } | Ruft den Stil der ersten Spalte ab. |
| [FirstRow](../../aspose.words/conditionalstylecollection/firstrow/) { get; } | Ruft den Stil der ersten Zeile ab. |
| [Item](../../aspose.words/conditionalstylecollection/item/) { get; } | Ruft eine[`ConditionalStyle`](../conditionalstyle/) Objekt nach bedingtem Stiltyp. (2 indexers) |
| [LastColumn](../../aspose.words/conditionalstylecollection/lastcolumn/) { get; } | Ruft den Stil der letzten Spalte ab. |
| [LastRow](../../aspose.words/conditionalstylecollection/lastrow/) { get; } | Ruft den Stil der letzten Zeile ab. |
| [OddColumnBanding](../../aspose.words/conditionalstylecollection/oddcolumnbanding/) { get; } | Ruft den ungeraden Spaltenbandstil ab. |
| [OddRowBanding](../../aspose.words/conditionalstylecollection/oddrowbanding/) { get; } | Ruft den ungeraden Zeilenbandstil ab. |
| [TopLeftCell](../../aspose.words/conditionalstylecollection/topleftcell/) { get; } | Ruft den Zellenstil oben links ab. |
| [TopRightCell](../../aspose.words/conditionalstylecollection/toprightcell/) { get; } | Ruft den Zellenstil oben rechts ab. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [ClearFormatting](../../aspose.words/conditionalstylecollection/clearformatting/)() | Löscht alle bedingten Stile des Tabellenstils. |
| [GetEnumerator](../../aspose.words/conditionalstylecollection/getenumerator/)() | Gibt ein Enumeratorobjekt zurück, mit dem alle bedingten Stile in der Sammlung durchlaufen werden können. |

## Bemerkungen

Es ist nicht möglich, Elemente zu dieser Sammlung hinzuzufügen oder daraus zu entfernen. Sie enthält einen permanenten Satz von Elementen: ein Element für jeden Wert des[`ConditionalStyleType`](../conditionalstyletype/) Aufzählungstyp.

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

* class [ConditionalStyle](../conditionalstyle/)
* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)
