---
title: DefaultParagraphFormat
second_title: Aspose.Words för .NET API Referens
description: Får dokumentets standardstyckeformatering.
type: docs
weight: 30
url: /sv/net/aspose.words/stylecollection/defaultparagraphformat/
---
## StyleCollection.DefaultParagraphFormat property

Får dokumentets standardstyckeformatering.

```csharp
public ParagraphFormat DefaultParagraphFormat { get; }
```

### Anmärkningar

Observera att dokumentomfattande standardinställningar introducerades i Microsoft Word 2007 och stöds fullt ut i OOXML-format (Docx) only. Tidigare dokumentformat har inget stöd för dokumentets standardstyckeformatering.

### Exempel

Visar hur man lägger till en stil till ett dokuments stilsamling.

```csharp
Document doc = new Document();
StyleCollection styles = doc.Styles;

// Ställ in standardparametrar för nya stilar som vi senare kan lägga till i den här samlingen.
styles.DefaultFont.Name = "Courier New";

// Om vi lägger till en stil av "StyleType.Paragraph", kommer samlingen att tillämpa värdena för
// dess "DefaultParagraphFormat"-egenskap till stilens "ParagraphFormat"-egenskap.
styles.DefaultParagraphFormat.FirstLineIndent = 15.0;

// Lägg till en stil och kontrollera sedan att den har standardinställningarna.
styles.Add(StyleType.Paragraph, "MyStyle");

Assert.AreEqual("Courier New", styles[4].Font.Name);
Assert.AreEqual(15.0, styles["MyStyle"].ParagraphFormat.FirstLineIndent);
```

### Se även

* class [ParagraphFormat](../../paragraphformat)
* class [StyleCollection](../../stylecollection)
* namnutrymme [Aspose.Words](../../stylecollection)
* hopsättning [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->