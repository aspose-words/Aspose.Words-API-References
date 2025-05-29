---
title: ShapeBase.AllowOverlap
linktitle: AllowOverlap
articleTitle: AllowOverlap
second_title: Aspose.Words per .NET
description: Scopri la proprietà ShapeBase AllowOverlap, controlla le interazioni delle forme abilitando o disabilitando la sovrapposizione con altre forme per una maggiore flessibilità di progettazione.
type: docs
weight: 10
url: /it/net/aspose.words.drawing/shapebase/allowoverlap/
---
## ShapeBase.AllowOverlap property

Ottiene o imposta un valore che specifica se questa forma può sovrapporsi ad altre forme.

```csharp
public bool AllowOverlap { get; set; }
```

## Osservazioni

Questa proprietà influenza il comportamento della forma in Microsoft Word. Aspose.Words ignora il valore di questa proprietà.

Questa proprietà è applicabile solo alle forme di livello superiore.

Il valore predefinito è`VERO`.

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

* class [ShapeBase](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
