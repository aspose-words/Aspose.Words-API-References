---
title: Table.AllowOverlap
second_title: Aspose.Words per .NET API Reference
description: Table proprietà. Ottiene se una tabella mobile deve consentire ad altri oggetti mobili nel documento di sovrapporsi alle sue estensioni quando viene visualizzata. Il valore predefinito èVERO .
type: docs
weight: 70
url: /it/net/aspose.words.tables/table/allowoverlap/
---
## Table.AllowOverlap property

Ottiene se una tabella mobile deve consentire ad altri oggetti mobili nel documento di sovrapporsi alle sue estensioni quando viene visualizzata. Il valore predefinito è`VERO` .

```csharp
public bool AllowOverlap { get; }
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

* class [Table](../)
* spazio dei nomi [Aspose.Words.Tables](../../table/)
* assemblea [Aspose.Words](../../../)


