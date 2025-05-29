---
title: Table.AllowOverlap
linktitle: AllowOverlap
articleTitle: AllowOverlap
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „Tabellenüberlappung zulassen“, die steuert, ob schwebende Objekte Ihre Tabelle überlappen können. Verbessern Sie die Layoutflexibilität für eine bessere Dokumentpräsentation.
type: docs
weight: 70
url: /de/net/aspose.words.tables/table/allowoverlap/
---
## Table.AllowOverlap property

Gibt an, ob eine schwebende Tabelle anderen schwebenden Objekten im Dokument erlauben soll, ihre Ausdehnungen bei der Anzeige zu überlappen. Der Standardwert ist`WAHR` .

```csharp
public bool AllowOverlap { get; }
```

## Beispiele

Zeigt, wie mit den Eigenschaften schwebender Tabellen gearbeitet wird.

```csharp
Document doc = new Document(MyDir + "Table wrapped by text.docx");

Table table = doc.FirstSection.Body.Tables[0];

if (table.TextWrapping == TextWrapping.Around)
{
    Assert.AreEqual(RelativeHorizontalPosition.Margin, table.HorizontalAnchor);
    Assert.AreEqual(RelativeVerticalPosition.Paragraph, table.VerticalAnchor);
    Assert.AreEqual(false, table.AllowOverlap);

    // Für den HorizontalAnchor-Setter sind in RelativeHorizontalPosition nur Margin, Page und Column verfügbar.
    // Für alle anderen Werte wird die ArgumentException ausgelöst.
    table.HorizontalAnchor = RelativeHorizontalPosition.Column;

    // Für den VerticalAnchor-Setter sind in RelativeVerticalPosition nur Margin, Page und Paragraph verfügbar.
    // Für alle anderen Werte wird die ArgumentException ausgelöst.
    table.VerticalAnchor = RelativeVerticalPosition.Page;
}
```

### Siehe auch

* class [Table](../)
* namensraum [Aspose.Words.Tables](../../../aspose.words.tables/)
* Montage [Aspose.Words](../../../)
