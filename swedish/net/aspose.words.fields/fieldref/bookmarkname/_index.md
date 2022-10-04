---
title: BookmarkName
second_title: Aspose.Words för .NET API Referens
description: Hämtar eller ställer in det refererade bokmärkets namn.
type: docs
weight: 20
url: /sv/net/aspose.words.fields/fieldref/bookmarkname/
---
## FieldRef.BookmarkName property

Hämtar eller ställer in det refererade bokmärkets namn.

```csharp
public string BookmarkName { get; set; }
```

### Exempel

Visar hur man skapar bokmärkt text med ett SET-fält och sedan visar det i dokumentet med ett REF-fält.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

  // Namnge bokmärkt text med ett SET-fält.
// Detta fält hänvisar till "bokmärket" inte en bokmärkesstruktur som visas i texten, utan en namngiven variabel.
FieldSet fieldSet = (FieldSet)builder.InsertField(FieldType.FieldSet, false);
fieldSet.BookmarkName = "MyBookmark";
fieldSet.BookmarkText = "Hello world!";
fieldSet.Update();

Assert.AreEqual(" SET  MyBookmark \"Hello world!\"", fieldSet.GetFieldCode());

// Referera till bokmärket efter namn i ett REF-fält och visa dess innehåll.
FieldRef fieldRef = (FieldRef)builder.InsertField(FieldType.FieldRef, true);
fieldRef.BookmarkName = "MyBookmark";
fieldRef.Update();

Assert.AreEqual(" REF  MyBookmark", fieldRef.GetFieldCode());
Assert.AreEqual("Hello world!", fieldRef.Result);

doc.Save(ArtifactsDir + "Field.SET.REF.docx");
```

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

    // Vi kommer att tillämpa ett anpassat listformat, där antalet vinkelparenteser anger vilken listnivå vi för närvarande befinner oss på.
    builder.ListFormat.ApplyNumberDefault();
    builder.ListFormat.ListLevel.NumberFormat = "> \x0000";

    // Infoga ett REF-fält som kommer att innehålla texten i vårt bokmärke, fungera som en hyperlänk och klona bokmärkets fotnoter.
    FieldRef field = InsertFieldRef(builder, "MyBookmark", "", "\n");
    field.IncludeNoteOrComment = true;
    field.InsertHyperlink = true;

    Assert.AreEqual(" REF  MyBookmark \\f \\h", field.GetFieldCode());

    // Infoga ett REF-fält och visa om det refererade bokmärket är ovanför eller under det.
    field = InsertFieldRef(builder, "MyBookmark", "The referenced paragraph is ", " this field.\n");
    field.InsertRelativePosition = true;

    Assert.AreEqual(" REF  MyBookmark \\p", field.GetFieldCode());

    // Visa listnumret för bokmärket som det visas i dokumentet.
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

    // Visa bokmärkets listnummer och numren för alla listnivåer ovanför det.
    field = InsertFieldRef(builder, "MyBookmark", "The bookmark's full context paragraph number is ", "\n");
    field.InsertParagraphNumberInFullContext = true;

    Assert.AreEqual(" REF  MyBookmark \\w", field.GetFieldCode());

    builder.InsertBreak(BreakType.PageBreak);

    // Visa listnivånumren mellan detta REF-fält och bokmärket som det refererar till.
    field = InsertFieldRef(builder, "MyBookmark", "The bookmark's relative paragraph number is ", "\n");
    field.InsertParagraphNumberInRelativeContext = true;

    Assert.AreEqual(" REF  MyBookmark \\r", field.GetFieldCode());

    // I slutet av dokumentet kommer bokmärket att visas som ett listobjekt här.
    builder.Writeln("List level above bookmark");
    builder.ListFormat.ListLevelNumber++;
    builder.ListFormat.ListLevel.NumberFormat = ">>> \x0002";

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.REF.docx");

/// <summary>
/// Få dokumentbyggaren att infoga ett REF-fält, referera till ett bokmärke med det och lägg till text före och efter det.
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
* namnutrymme [Aspose.Words.Fields](../../fieldref/)
* hopsättning [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
