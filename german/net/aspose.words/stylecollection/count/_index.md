---
title: StyleCollection.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words für .NET
description: StyleCollection Count eigendom. Ruft die Anzahl der Stile in der Sammlung ab in C#.
type: docs
weight: 10
url: /de/net/aspose.words/stylecollection/count/
---
## StyleCollection.Count property

Ruft die Anzahl der Stile in der Sammlung ab.

```csharp
public int Count { get; }
```

## Beispiele

Zeigt, wie man der Stilsammlung eines Dokuments einen Stil hinzufügt.

```csharp
Document doc = new Document();

StyleCollection styles = doc.Styles;
// Standardparameter für neue Stile festlegen, die wir später möglicherweise zu dieser Sammlung hinzufügen.
styles.DefaultFont.Name = "Courier New";
// Wenn wir einen Stil von „StyleType.Paragraph“ hinzufügen, wendet die Sammlung die Werte von an
// seine „DefaultParagraphFormat“-Eigenschaft zur „ParagraphFormat“-Eigenschaft des Stils.
styles.DefaultParagraphFormat.FirstLineIndent = 15.0;
// Fügen Sie einen Stil hinzu und überprüfen Sie dann, ob er die Standardeinstellungen hat.
styles.Add(StyleType.Paragraph, "MyStyle");

Assert.AreEqual("Courier New", styles[4].Font.Name);
Assert.AreEqual(15.0, styles["MyStyle"].ParagraphFormat.FirstLineIndent);
```

### Siehe auch

* class [StyleCollection](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
