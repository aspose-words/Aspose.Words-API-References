---
title: FieldRef.InsertParagraphNumberInFullContext
linktitle: InsertParagraphNumberInFullContext
articleTitle: InsertParagraphNumberInFullContext
second_title: Aspose.Words för .NET
description: Styr styckenumrering med egenskapen FieldRef InsertParagraphNumberInFullContext. Hantera enkelt referenser för förbättrad dokumenttydlighet.
type: docs
weight: 60
url: /sv/net/aspose.words.fields/fieldref/insertparagraphnumberinfullcontext/
---
## FieldRef.InsertParagraphNumberInFullContext property

Hämtar eller anger om styckets nummer för det refererade stycket ska infogas i full kontext.

```csharp
public bool InsertParagraphNumberInFullContext { get; set; }
```

## Exempel

Visar hur man infogar REF-fält för att referera till bokmärken.

```csharp
public void FieldRef()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.StartBookmark("MyBookmark");
    builder.InsertFootnote(FootnoteType.Footnote, "MyBookmark footnote #1");
    builder.Write("Text that will appear in REF field");
    builder.InsertFootnote(FootnoteType.Footnote, "MyBookmark footnote #2");
    builder.EndBookmark("MyBookmark");
    builder.MoveToDocumentStart();

    // Vi kommer att använda ett anpassat listformat, där antalet vinkelparenteser anger listnivån vi befinner oss på för närvarande.
    builder.ListFormat.ApplyNumberDefault();
    builder.ListFormat.ListLevel.NumberFormat = "> \x0000";

    // Infoga ett REF-fält som ska innehålla texten i vårt bokmärke, fungera som en hyperlänk och klona bokmärkets fotnoter.
    FieldRef field = InsertFieldRef(builder, "MyBookmark", "", "\n");
    field.IncludeNoteOrComment = true;
    field.InsertHyperlink = true;

    Assert.AreEqual(" REF  MyBookmark \\f \\h", field.GetFieldCode());

    // Infoga ett REF-fält och visa om det refererade bokmärket är ovanför eller under det.
    field = InsertFieldRef(builder, "MyBookmark", "The referenced paragraph is ", " this field.\n");
    field.InsertRelativePosition = true;

    Assert.AreEqual(" REF  MyBookmark \\p", field.GetFieldCode());

    // Visa bokmärkets listnummer som det visas i dokumentet.
    field = InsertFieldRef(builder, "MyBookmark", "The bookmark's paragraph number is ", "\n");
    field.InsertParagraphNumber = true;

    Assert.AreEqual(" REF  MyBookmark \\n", field.GetFieldCode());

    // Visa bokmärkets listnummer, men med icke-avgränsande tecken, såsom vinkelparenteser, utelämnade.
    field = InsertFieldRef(builder, "MyBookmark", "The bookmark's paragraph number, non-delimiters suppressed, is ", "\n");
    field.InsertParagraphNumber = true;
    field.SuppressNonDelimiters = true;

    Assert.AreEqual(" REF  MyBookmark \\n \\t", field.GetFieldCode());

    // Flytta ner en listnivå.
    builder.ListFormat.ListLevelNumber++;
    builder.ListFormat.ListLevel.NumberFormat = ">> \x0001";

    // Visar bokmärkets listnummer och numren för alla listnivåer ovanför det.
    field = InsertFieldRef(builder, "MyBookmark", "The bookmark's full context paragraph number is ", "\n");
    field.InsertParagraphNumberInFullContext = true;

    Assert.AreEqual(" REF  MyBookmark \\w", field.GetFieldCode());

    builder.InsertBreak(BreakType.PageBreak);

    // Visar listnivånumren mellan detta REF-fält och bokmärket som det refererar till.
    field = InsertFieldRef(builder, "MyBookmark", "The bookmark's relative paragraph number is ", "\n");
    field.InsertParagraphNumberInRelativeContext = true;

    Assert.AreEqual(" REF  MyBookmark \\r", field.GetFieldCode());

    // I slutet av dokumentet visas bokmärket som ett listobjekt här.
    builder.Writeln("List level above bookmark");
    builder.ListFormat.ListLevelNumber++;
    builder.ListFormat.ListLevel.NumberFormat = ">>> \x0002";

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.REF.docx");
}

/// <summary>
/// Få dokumentbyggaren att infoga ett REF-fält, referera till ett bokmärke med det och lägga till text före och efter det.
/// </summary>
private static FieldRef InsertFieldRef(DocumentBuilder builder, string bookmarkName, string textBefore, string textAfter)
{
    builder.Write(textBefore);
    FieldRef field = (FieldRef)builder.InsertField(FieldType.FieldRef, true);
    field.BookmarkName = bookmarkName;
    builder.Write(textAfter);
    return field;
}
```

### Se även

* class [FieldRef](../)
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)
