---
title: TableStyle.ColumnStripe
linktitle: ColumnStripe
articleTitle: ColumnStripe
second_title: Aspose.Words für .NET
description: Entdecken Sie die TableStyle ColumnStripe-Eigenschaft, um die Abgrenzung gerader/ungerader Spalten einfach anzupassen und Ihren Tabellen ein elegantes, professionelles Aussehen zu verleihen.
type: docs
weight: 70
url: /de/net/aspose.words/tablestyle/columnstripe/
---
## TableStyle.ColumnStripe property

Ruft die Anzahl der Spalten ab oder legt sie fest, die in die Bänder einbezogen werden sollen, wenn der Stil Bänder für gerade/ungerade Spalten vorgibt.

```csharp
public int ColumnStripe { get; set; }
```

## Beispiele

Zeigt, wie bedingte Tabellenstile erstellt werden, die zwischen Zeilen wechseln.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Wir können einen bedingten Stil einer Tabelle konfigurieren, um der Zeile/Spalte eine andere Farbe zuzuweisen,
// basierend darauf, ob die Zeile/Spalte gerade oder ungerade ist, wodurch ein abwechselndes Farbmuster entsteht.
// Wir können auch eine Zahl n auf die Zeilen-/Spaltenbandierung anwenden,
// was bedeutet, dass die Farbe nach jeweils n Zeilen/Spalten statt nach einer wechselt.
// Erstellen Sie eine Tabelle, in der einzelne Spalten und Zeilen zusammengefasst werden, die Spalten werden in Dreiergruppen zusammengefasst.
Table table = builder.StartTable();
for (int i = 0; i < 15; i++)
{
    for (int j = 0; j < 4; j++)
    {
        builder.InsertCell();
        builder.Writeln($"{(j % 2 == 0 ? "Even" : "Odd")} column.");
        builder.Write($"Row banding {(i % 3 == 0 ? "start" : "continuation")}.");
    }
    builder.EndRow();
}
builder.EndTable();

// Wenden Sie einen Linienstil auf alle Ränder der Tabelle an.
TableStyle tableStyle = (TableStyle)doc.Styles.Add(StyleType.Table, "MyTableStyle1");
tableStyle.Borders.Color = Color.Black;
tableStyle.Borders.LineStyle = LineStyle.Double;

// Legen Sie die beiden Farben fest, die alle 3 Zeilen abwechseln.
tableStyle.RowStripe = 3;
tableStyle.ConditionalStyles[ConditionalStyleType.OddRowBanding].Shading.BackgroundPatternColor = Color.LightBlue;
tableStyle.ConditionalStyles[ConditionalStyleType.EvenRowBanding].Shading.BackgroundPatternColor = Color.LightCyan;

// Legen Sie eine Farbe fest, die auf jede gerade Spalte angewendet werden soll. Dadurch wird jede benutzerdefinierte Zeilenfärbung überschrieben.
tableStyle.ColumnStripe = 1;
tableStyle.ConditionalStyles[ConditionalStyleType.EvenColumnBanding].Shading.BackgroundPatternColor = Color.LightSalmon;

table.Style = tableStyle;

// Die Eigenschaft „StyleOptions“ aktiviert standardmäßig die Zeilenbandbildung.
Assert.AreEqual(TableStyleOptions.FirstRow | TableStyleOptions.FirstColumn | TableStyleOptions.RowBands,
    table.StyleOptions);

// Verwenden Sie die Eigenschaft „StyleOptions“, um auch die Spaltenbandbildung zu aktivieren.
table.StyleOptions = table.StyleOptions | TableStyleOptions.ColumnBands;

doc.Save(ArtifactsDir + "Table.AlternatingRowStyles.docx");
```

### Siehe auch

* class [TableStyle](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
