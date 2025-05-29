---
title: StyleCollection.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „StyleCollection Count“, um ganz einfach die Gesamtzahl der Stile in Ihrer Sammlung abzurufen und so die Organisation und Verwaltung zu verbessern.
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

Zeigt, wie der Stilsammlung eines Dokuments ein Stil hinzugefügt wird.

```csharp
Document doc = new Document();

StyleCollection styles = doc.Styles;
// Legen Sie Standardparameter für neue Stile fest, die wir dieser Sammlung später hinzufügen können.
styles.DefaultFont.Name = "Courier New";
// Wenn wir einen Stil vom Typ "StyleType.Paragraph" hinzufügen, wendet die Sammlung die Werte von
// seine Eigenschaft „DefaultParagraphFormat“ zur Eigenschaft „ParagraphFormat“ des Stils.
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
