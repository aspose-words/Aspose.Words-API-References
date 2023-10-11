---
title: Table.VerticalAnchor
second_title: Aspose.Words per .NET API Reference
description: Table proprietà. Ottiene loggetto base da cui deve essere calcolato il posizionamento verticale della tabella mobile. Il valore predefinito èMargin .
type: docs
weight: 340
url: /it/net/aspose.words.tables/table/verticalanchor/
---
## Table.VerticalAnchor property

Ottiene l'oggetto base da cui deve essere calcolato il posizionamento verticale della tabella mobile. Il valore predefinito èMargin .

```csharp
public RelativeVerticalPosition VerticalAnchor { get; set; }
```

### Esempi

Mostra come utilizzare le proprietà delle tabelle mobili.

```csharp
Document doc = new Document(MyDir + "Table wrapped by text.docx");

Table table = doc.FirstSection.Body.Tables[0];

if (table.TextWrapping == TextWrapping.Around)
{
    Assert.AreEqual(RelativeHorizontalPosition.Margin, table.HorizontalAnchor);
    Assert.AreEqual(RelativeVerticalPosition.Paragraph, table.VerticalAnchor);
    Assert.AreEqual(false, table.AllowOverlap);

    // Solo margine, pagina e colonna disponibili in RelativeHorizontalPosition per il setter orizzontali.
    // L'ArgumentException verrà generata per qualsiasi altro valore.
    table.HorizontalAnchor = RelativeHorizontalPosition.Column;

    // Solo margine, pagina e paragrafo disponibili in RelativeVerticalPosition per il setter VerticalAnchor.
    // L'ArgumentException verrà generata per qualsiasi altro valore.
    table.VerticalAnchor = RelativeVerticalPosition.Page;
}
```

### Guarda anche

* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* class [Table](../)
* spazio dei nomi [Aspose.Words.Tables](../../table/)
* assemblea [Aspose.Words](../../../)


