---
title: StyleCollection.DefaultParagraphFormat
linktitle: DefaultParagraphFormat
articleTitle: DefaultParagraphFormat
second_title: Aspose.Words für .NET
description: StyleCollection DefaultParagraphFormat eigendom. Ruft die standardmäßige Absatzformatierung des Dokuments ab in C#.
type: docs
weight: 30
url: /de/net/aspose.words/stylecollection/defaultparagraphformat/
---
## StyleCollection.DefaultParagraphFormat property

Ruft die standardmäßige Absatzformatierung des Dokuments ab.

```csharp
public ParagraphFormat DefaultParagraphFormat { get; }
```

## Bemerkungen

Beachten Sie, dass dokumentweite Standardeinstellungen in Microsoft Word 2007 eingeführt wurden und in OOXML-Formaten vollständig unterstützt werden (Docx) only. Frühere Dokumentformate unterstützen die standardmäßige Absatzformatierung des Dokuments nicht.

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

* class [ParagraphFormat](../../paragraphformat/)
* class [StyleCollection](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
