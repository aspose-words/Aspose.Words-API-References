---
title: StyleCollection.DefaultFont
linktitle: DefaultFont
articleTitle: DefaultFont
second_title: Aspose.Words för .NET
description: Upptäck egenskapen StyleCollection DefaultFont för sömlös textformatering i dokument. Förbättra dina dokument med en konsekvent och professionell stil.
type: docs
weight: 20
url: /sv/net/aspose.words/stylecollection/defaultfont/
---
## StyleCollection.DefaultFont property

Hämtar standardtextformatering för dokumentet.

```csharp
public Font DefaultFont { get; }
```

## Anmärkningar

Observera att dokumentomfattande standardinställningar introducerades i Microsoft Word 2007 och stöds fullt ut i OOXML-format (Docx) endast. Tidigare dokumentformat har begränsat stöd för den här funktionen och endast teckensnittsnamn kan lagras.

## Exempel

Visar hur man lägger till en stil i ett dokuments stilsamling.

```csharp
Document doc = new Document();

StyleCollection styles = doc.Styles;
// Ange standardparametrar för nya stilar som vi senare kan lägga till i den här samlingen.
styles.DefaultFont.Name = "Courier New";
// Om vi lägger till en stil av typen "StyleType.Paragraph" kommer samlingen att tillämpa värdena för
// dess "DefaultParagraphFormat"-egenskap till stilens "ParagraphFormat"-egenskap.
styles.DefaultParagraphFormat.FirstLineIndent = 15.0;
// Lägg till en stil och kontrollera sedan att den har standardinställningarna.
styles.Add(StyleType.Paragraph, "MyStyle");

Assert.AreEqual("Courier New", styles[4].Font.Name);
Assert.AreEqual(15.0, styles["MyStyle"].ParagraphFormat.FirstLineIndent);
```

### Se även

* class [Font](../../font/)
* class [StyleCollection](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
