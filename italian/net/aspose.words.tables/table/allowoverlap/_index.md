---
title: Table.AllowOverlap
linktitle: AllowOverlap
articleTitle: AllowOverlap
second_title: Aspose.Words per .NET
description: Scopri la proprietà Table AllowOverlap, che controlla se gli oggetti mobili possono sovrapporsi alla tabella. Aumenta la flessibilità del layout per una migliore presentazione dei documenti.
type: docs
weight: 70
url: /it/net/aspose.words.tables/table/allowoverlap/
---
## Table.AllowOverlap property

Ottiene se una tabella mobile deve consentire ad altri oggetti mobili nel documento di sovrapporsi alle sue estensioni quando vengono visualizzati. Il valore predefinito è `VERO` .

```csharp
public bool AllowOverlap { get; }
```

## Esempi

Mostra come lavorare con le proprietà delle tabelle mobili.

```csharp
Document doc = new Document(MyDir + "Table wrapped by text.docx");

Table table = doc.FirstSection.Body.Tables[0];

if (table.TextWrapping == TextWrapping.Around)
{
    Assert.AreEqual(RelativeHorizontalPosition.Margin, table.HorizontalAnchor);
    Assert.AreEqual(RelativeVerticalPosition.Paragraph, table.VerticalAnchor);
    Assert.AreEqual(false, table.AllowOverlap);

    // Solo Margine, Pagina, Colonna disponibili in RelativeHorizontalPosition per il setter HorizontalAnchor.
    // L'eccezione ArgumentException verrà generata per tutti gli altri valori.
    table.HorizontalAnchor = RelativeHorizontalPosition.Column;

    // Solo Margine, Pagina, Paragrafo disponibili in RelativeVerticalPosition per il setter VerticalAnchor.
    // L'eccezione ArgumentException verrà generata per tutti gli altri valori.
    table.VerticalAnchor = RelativeVerticalPosition.Page;
}
```

### Guarda anche

* class [Table](../)
* spazio dei nomi [Aspose.Words.Tables](../../../aspose.words.tables/)
* assemblea [Aspose.Words](../../../)
