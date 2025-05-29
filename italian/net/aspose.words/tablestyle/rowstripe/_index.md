---
title: TableStyle.RowStripe
linktitle: RowStripe
articleTitle: RowStripe
second_title: Aspose.Words per .NET
description: Scopri la proprietà TableStyle RowStripe per personalizzare facilmente la suddivisione in fasce delle righe pari/dispari, migliorando la leggibilità della tabella e l'aspetto visivo.
type: docs
weight: 120
url: /it/net/aspose.words/tablestyle/rowstripe/
---
## TableStyle.RowStripe property

Ottiene o imposta un numero di righe da includere nella suddivisione in bande quando lo stile specifica la suddivisione in bande di righe pari/dispari.

```csharp
public int RowStripe { get; set; }
```

## Esempi

Mostra come creare stili di tabella condizionali che si alternano tra le righe.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Possiamo configurare uno stile condizionale di una tabella per applicare un colore diverso alla riga/colonna,
// in base al fatto che la riga/colonna sia pari o dispari, creando uno schema di colori alternati.
// Possiamo anche applicare un numero n alla suddivisione in fasce di riga/colonna,
// significa che il colore si alterna dopo ogni n righe/colonne anziché una.
// Crea una tabella in cui le singole colonne e righe verranno raggruppate e le colonne verranno raggruppate in gruppi di tre.
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

// Applica uno stile di linea a tutti i bordi della tabella.
TableStyle tableStyle = (TableStyle)doc.Styles.Add(StyleType.Table, "MyTableStyle1");
tableStyle.Borders.Color = Color.Black;
tableStyle.Borders.LineStyle = LineStyle.Double;

// Imposta i due colori, che si alterneranno ogni 3 righe.
tableStyle.RowStripe = 3;
tableStyle.ConditionalStyles[ConditionalStyleType.OddRowBanding].Shading.BackgroundPatternColor = Color.LightBlue;
tableStyle.ConditionalStyles[ConditionalStyleType.EvenRowBanding].Shading.BackgroundPatternColor = Color.LightCyan;

// Imposta un colore da applicare a ogni colonna pari, che sovrascriverà qualsiasi colorazione di riga personalizzata.
tableStyle.ColumnStripe = 1;
tableStyle.ConditionalStyles[ConditionalStyleType.EvenColumnBanding].Shading.BackgroundPatternColor = Color.LightSalmon;

table.Style = tableStyle;

// La proprietà "StyleOptions" abilita per impostazione predefinita la suddivisione in fasce delle righe.
Assert.AreEqual(TableStyleOptions.FirstRow | TableStyleOptions.FirstColumn | TableStyleOptions.RowBands,
    table.StyleOptions);

// Utilizzare la proprietà "StyleOptions" anche per abilitare la suddivisione in bande di colonne.
table.StyleOptions = table.StyleOptions | TableStyleOptions.ColumnBands;

doc.Save(ArtifactsDir + "Table.AlternatingRowStyles.docx");
```

### Guarda anche

* class [TableStyle](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
