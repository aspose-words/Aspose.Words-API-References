---
title: Table.AllowOverlap
linktitle: AllowOverlap
articleTitle: AllowOverlap
second_title: Aspose.Words per .NET
description: Table AllowOverlap proprietà. Indica se una tabella mobile deve consentire ad altri oggetti mobili nel documento di sovrapporsi alle sue estensioni quando viene visualizzato. Il valore predefinito èVERO  in C#.
type: docs
weight: 70
url: /it/net/aspose.words.tables/table/allowoverlap/
---
## Table.AllowOverlap property

Indica se una tabella mobile deve consentire ad altri oggetti mobili nel documento di sovrapporsi alle sue estensioni quando viene visualizzato. Il valore predefinito è`VERO` .

```csharp
public bool AllowOverlap { get; }
```

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

* class [Table](../)
* spazio dei nomi [Aspose.Words.Tables](../../../aspose.words.tables/)
* assemblea [Aspose.Words](../../../)
