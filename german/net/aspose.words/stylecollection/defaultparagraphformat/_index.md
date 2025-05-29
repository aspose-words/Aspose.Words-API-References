---
title: StyleCollection.DefaultParagraphFormat
linktitle: DefaultParagraphFormat
articleTitle: DefaultParagraphFormat
second_title: Aspose.Words für .NET
description: Entdecken Sie die StyleCollection-Eigenschaft DefaultParagraphFormat, um einfach auf die Standardabsatzformatierung Ihres Dokuments zuzugreifen und diese für eine bessere Lesbarkeit anzupassen.
type: docs
weight: 30
url: /de/net/aspose.words/stylecollection/defaultparagraphformat/
---
## StyleCollection.DefaultParagraphFormat property

Ruft die Standardabsatzformatierung des Dokuments ab.

```csharp
public ParagraphFormat DefaultParagraphFormat { get; }
```

## Bemerkungen

Beachten Sie, dass dokumentweite Standardeinstellungen in Microsoft Word 2007 eingeführt wurden und in OOXML-Formaten vollständig unterstützt werden (Docx) nur. Frühere Dokumentformate unterstützen die standardmäßige Absatzformatierung von Dokumenten nicht.

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

* class [ParagraphFormat](../../paragraphformat/)
* class [StyleCollection](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
