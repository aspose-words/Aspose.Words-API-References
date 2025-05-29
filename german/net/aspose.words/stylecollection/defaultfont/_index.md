---
title: StyleCollection.DefaultFont
linktitle: DefaultFont
articleTitle: DefaultFont
second_title: Aspose.Words für .NET
description: Entdecken Sie die StyleCollection DefaultFont-Eigenschaft für eine nahtlose Textformatierung in Dokumenten. Optimieren Sie Ihre Dokumente mit einem einheitlichen, professionellen Stil.
type: docs
weight: 20
url: /de/net/aspose.words/stylecollection/defaultfont/
---
## StyleCollection.DefaultFont property

Ruft die Standardtextformatierung des Dokuments ab.

```csharp
public Font DefaultFont { get; }
```

## Bemerkungen

Beachten Sie, dass dokumentweite Standardeinstellungen in Microsoft Word 2007 eingeführt wurden und in OOXML-Formaten vollständig unterstützt werden (Docx) nur. Frühere Dokumentformate unterstützen diese Funktion nur eingeschränkt und es können nur Schriftartnamen gespeichert werden.

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

* class [Font](../../font/)
* class [StyleCollection](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
