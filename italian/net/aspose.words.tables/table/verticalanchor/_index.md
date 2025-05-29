---
title: Table.VerticalAnchor
linktitle: VerticalAnchor
articleTitle: VerticalAnchor
second_title: Aspose.Words per .NET
description: Scopri la proprietà Table VerticalAnchor per ottimizzare il posizionamento delle tabelle mobili. Scopri come migliorare il controllo del layout con il valore predefinito Margin.
type: docs
weight: 340
url: /it/net/aspose.words.tables/table/verticalanchor/
---
## Table.VerticalAnchor property

Ottiene l'oggetto base da cui deve essere calcolato il posizionamento verticale della tabella mobile. Il valore predefinito èMargin .

```csharp
public RelativeVerticalPosition VerticalAnchor { get; set; }
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

* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* class [Table](../)
* spazio dei nomi [Aspose.Words.Tables](../../../aspose.words.tables/)
* assemblea [Aspose.Words](../../../)
