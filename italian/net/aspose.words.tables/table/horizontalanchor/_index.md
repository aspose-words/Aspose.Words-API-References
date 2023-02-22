---
title: Table.HorizontalAnchor
second_title: Aspose.Words per .NET API Reference
description: Table proprietà. Ottiene loggetto base da cui calcolare il posizionamento orizzontale della tabella mobile. Il valore predefinito èColumn .
type: docs
weight: 170
url: /it/net/aspose.words.tables/table/horizontalanchor/
---
## Table.HorizontalAnchor property

Ottiene l'oggetto base da cui calcolare il posizionamento orizzontale della tabella mobile. Il valore predefinito èColumn .

```csharp
public RelativeHorizontalPosition HorizontalAnchor { get; set; }
```

### Esempi

Mostra come lavorare con le proprietà delle tabelle mobili.

```csharp
Document doc = new Document(MyDir + "Table wrapped by text.docx");

Table table = doc.FirstSection.Body.Tables[0];

if (table.TextWrapping == TextWrapping.Around)
{
    Assert.AreEqual(RelativeHorizontalPosition.Margin, table.HorizontalAnchor);
    Assert.AreEqual(RelativeVerticalPosition.Paragraph, table.VerticalAnchor);
    Assert.AreEqual(false, table.AllowOverlap);

    // Solo margine, pagina, colonna disponibile in RelativeHorizontalPosition per il setter di ancoraggio orizzontale.
    // Verrà generata ArgumentException per qualsiasi altro valore.
    table.HorizontalAnchor = RelativeHorizontalPosition.Column;

    // Solo margine, pagina, paragrafo disponibile in posizione verticale relativa per il setter di ancoraggio verticale.
    // Verrà generata ArgumentException per qualsiasi altro valore.
    table.VerticalAnchor = RelativeVerticalPosition.Page;
}
```

### Guarda anche

* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* class [Table](../)
* spazio dei nomi [Aspose.Words.Tables](../../table/)
* assemblea [Aspose.Words](../../../)


