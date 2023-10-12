---
title: StyleCollection.DefaultFont
second_title: Aspose.Words für .NET-API-Referenz
description: StyleCollection eigendom. Ruft die Standardtextformatierung des Dokuments ab.
type: docs
weight: 20
url: /de/net/aspose.words/stylecollection/defaultfont/
---
## StyleCollection.DefaultFont property

Ruft die Standardtextformatierung des Dokuments ab.

```csharp
public Font DefaultFont { get; }
```

### Bemerkungen

Beachten Sie, dass dokumentweite Standardeinstellungen in Microsoft Word 2007 eingeführt wurden und in OOXML-Formaten vollständig unterstützt werden (Docx) only. Frühere Dokumentformate unterstützen diese Funktion nur eingeschränkt und es können nur Schriftartnamen gespeichert werden.

### Beispiele

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

* class [Font](../../font/)
* class [StyleCollection](../)
* namensraum [Aspose.Words](../../stylecollection/)
* Montage [Aspose.Words](../../../)


