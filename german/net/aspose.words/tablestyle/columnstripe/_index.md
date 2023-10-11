---
title: TableStyle.ColumnStripe
second_title: Aspose.Words für .NET-API-Referenz
description: TableStyle eigendom. Ruft eine Anzahl von Spalten ab die in die Banderstellung einbezogen werden sollen oder legt diese fest wenn der Stil eine Banderstellung für ungerade/gerade Spalten vorgibt.
type: docs
weight: 70
url: /de/net/aspose.words/tablestyle/columnstripe/
---
## TableStyle.ColumnStripe property

Ruft eine Anzahl von Spalten ab, die in die Banderstellung einbezogen werden sollen, oder legt diese fest, wenn der Stil eine Banderstellung für ungerade/gerade Spalten vorgibt.

```csharp
public int ColumnStripe { get; set; }
```

### Beispiele

Zeigt, wie bedingte Tabellenstile erstellt werden, die zwischen Zeilen wechseln.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Wir können einen bedingten Stil einer Tabelle konfigurieren, um eine andere Farbe auf die Zeile/Spalte anzuwenden.
// basierend darauf, ob die Zeile/Spalte gerade oder ungerade ist, wodurch ein alternierendes Farbmuster entsteht.
// Wir können auch eine Zahl n auf die Zeilen-/Spaltenbandierung anwenden,
// bedeutet, dass die Farbe nach jeweils n Zeilen/Spalten statt nach einer wechselt.
// Erstellen Sie eine Tabelle, in der einzelne Spalten und Zeilen in drei Gruppen unterteilt werden.
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

// Einen Linienstil auf alle Ränder der Tabelle anwenden.
TableStyle tableStyle = (TableStyle)doc.Styles.Add(StyleType.Table, "MyTableStyle1");
tableStyle.Borders.Color = Color.Black;
tableStyle.Borders.LineStyle = LineStyle.Double;

// Legen Sie die beiden Farben fest, die sich alle 3 Zeilen abwechseln.
tableStyle.RowStripe = 3;
tableStyle.ConditionalStyles[ConditionalStyleType.OddRowBanding].Shading.BackgroundPatternColor = Color.LightBlue;
tableStyle.ConditionalStyles[ConditionalStyleType.EvenRowBanding].Shading.BackgroundPatternColor = Color.LightCyan;

// Legen Sie eine Farbe fest, die auf jede gerade Spalte angewendet wird und alle benutzerdefinierten Zeilenfarben überschreibt.
tableStyle.ColumnStripe = 1;
tableStyle.ConditionalStyles[ConditionalStyleType.EvenColumnBanding].Shading.BackgroundPatternColor = Color.LightSalmon;

table.Style = tableStyle;

// Die Eigenschaft „StyleOptions“ aktiviert standardmäßig die Zeilenbanderstellung.
Assert.AreEqual(TableStyleOptions.FirstRow | TableStyleOptions.FirstColumn | TableStyleOptions.RowBands,
    table.StyleOptions);

// Verwenden Sie die Eigenschaft „StyleOptions“ auch, um die Spaltenbänderung zu aktivieren.
table.StyleOptions = table.StyleOptions | TableStyleOptions.ColumnBands;

doc.Save(ArtifactsDir + "Table.AlternatingRowStyles.docx");
```

### Siehe auch

* class [TableStyle](../)
* namensraum [Aspose.Words](../../tablestyle/)
* Montage [Aspose.Words](../../../)


