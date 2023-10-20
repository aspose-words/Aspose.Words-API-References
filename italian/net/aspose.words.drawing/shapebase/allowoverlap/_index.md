---
title: ShapeBase.AllowOverlap
linktitle: AllowOverlap
articleTitle: AllowOverlap
second_title: Aspose.Words per .NET
description: ShapeBase AllowOverlap proprietà. Ottiene o imposta un valore che specifica se questa forma può sovrapporsi ad altre forme in C#.
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

Questa proprietà influisce sul comportamento della forma in Microsoft Word. Aspose.Words ignora il valore di questa proprietà.

Questa proprietà è applicabile solo alle forme di livello superiore.

Il valore predefinito è`VERO`.

## Esempi

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

* class [ShapeBase](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
