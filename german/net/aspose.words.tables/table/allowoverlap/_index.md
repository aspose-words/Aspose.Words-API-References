---
title: Table.AllowOverlap
second_title: Aspose.Words für .NET-API-Referenz
description: Table eigendom. Ruft ab ob eine schwebende Tabelle zulassen soll dass andere schwebende Objekte im Dokument ihre Grenzen überlappen wenn sie angezeigt werden. Der Standardwert istWAHR .
type: docs
weight: 70
url: /de/net/aspose.words.tables/table/allowoverlap/
---
## Table.AllowOverlap property

Ruft ab, ob eine schwebende Tabelle zulassen soll, dass andere schwebende Objekte im Dokument ihre Grenzen überlappen, wenn sie angezeigt werden. Der Standardwert ist`WAHR` .

```csharp
public bool AllowOverlap { get; }
```

### Beispiele

Zeigt, wie mit Floating-Table-Eigenschaften gearbeitet wird.

```csharp
Document doc = new Document(MyDir + "Table wrapped by text.docx");

Table table = doc.FirstSection.Body.Tables[0];

if (table.TextWrapping == TextWrapping.Around)
{
    Assert.AreEqual(RelativeHorizontalPosition.Margin, table.HorizontalAnchor);
    Assert.AreEqual(RelativeVerticalPosition.Paragraph, table.VerticalAnchor);
    Assert.AreEqual(false, table.AllowOverlap);

    // Nur Rand, Seite, Spalte in RelativeHorizontalPosition für HorizontalAnchor-Setter verfügbar.
    // Die ArgumentException wird für alle anderen Werte ausgelöst.
    table.HorizontalAnchor = RelativeHorizontalPosition.Column;

    // Nur Rand, Seite, Absatz verfügbar in RelativeVerticalPosition für VerticalAnchor-Setter.
    // Die ArgumentException wird für alle anderen Werte ausgelöst.
    table.VerticalAnchor = RelativeVerticalPosition.Page;
}
```

### Siehe auch

* class [Table](../)
* namensraum [Aspose.Words.Tables](../../table/)
* Montage [Aspose.Words](../../../)


