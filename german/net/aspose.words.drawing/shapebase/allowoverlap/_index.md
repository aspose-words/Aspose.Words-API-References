---
title: ShapeBase.AllowOverlap
linktitle: AllowOverlap
articleTitle: AllowOverlap
second_title: Aspose.Words für .NET
description: Entdecken Sie die ShapeBase AllowOverlap-Eigenschaft und steuern Sie Forminteraktionen, indem Sie die Überlappung mit anderen Formen aktivieren oder deaktivieren, um die Designflexibilität zu verbessern.
type: docs
weight: 10
url: /de/net/aspose.words.drawing/shapebase/allowoverlap/
---
## ShapeBase.AllowOverlap property

Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob diese Form andere Formen überlappen kann.

```csharp
public bool AllowOverlap { get; set; }
```

## Bemerkungen

Diese Eigenschaft beeinflusst das Verhalten der Form in Microsoft Word. Aspose.Words ignoriert den Wert dieser Eigenschaft.

Diese Eigenschaft ist nur auf Formen der obersten Ebene anwendbar.

Der Standardwert ist`WAHR`.

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

* class [ShapeBase](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
