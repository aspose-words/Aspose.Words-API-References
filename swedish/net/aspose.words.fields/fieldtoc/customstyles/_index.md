---
title: FieldToc.CustomStyles
second_title: Aspose.Words för .NET API Referens
description: FieldToc fast egendom. Hämtar eller ställer in en lista över andra stilar än de inbyggda rubrikstilarna som ska inkluderas i innehållsförteckningen.
type: docs
weight: 40
url: /sv/net/aspose.words.fields/fieldtoc/customstyles/
---
## FieldToc.CustomStyles property

Hämtar eller ställer in en lista över andra stilar än de inbyggda rubrikstilarna som ska inkluderas i innehållsförteckningen.

```csharp
public string CustomStyles { get; set; }
```

### Exempel

Visar hur man infogar en innehållsförteckning och fyller den med poster baserat på rubrikstilar.

```csharp
public void FieldToc()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.StartBookmark("MyBookmark");

    // Infoga ett innehållsförteckning-fält, som kommer att kompilera alla rubriker till en innehållsförteckning.
    // För varje rubrik kommer det här fältet att skapa en rad med texten i den rubrikstilen till vänster,
    // och sidan rubriken visas till höger.
    FieldToc field = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

    // Använd egenskapen BookmarkName för att bara lista rubriker
    // som visas inom gränserna för ett bokmärke med namnet "Mitt bokmärke".
    field.BookmarkName = "MyBookmark";

    // Text med en inbyggd rubrikstil, till exempel "Rubrik 1", som tillämpas på den kommer att räknas som en rubrik.
    // Vi kan namnge ytterligare stilar som ska plockas upp som rubriker av innehållsförteckningen i den här egenskapen och deras innehållsförteckningsnivåer.
    field.CustomStyles = "Quote; 6; Intense Quote; 7";

    // Som standard är Styles/TOC-nivåer separerade i CustomStyles-egenskapen med ett kommatecken,
    // men vi kan ställa in en anpassad avgränsare i den här egenskapen.
    doc.FieldOptions.CustomTocStyleSeparator = ";";

    // Konfigurera fältet för att utesluta alla rubriker som har innehållsförteckningsnivåer utanför detta intervall.
    field.HeadingLevelRange = "1-3";

    // Innehållsförteckningen visar inte sidnumren för rubriker vars innehållsförteckningsnivåer ligger inom detta intervall.
    field.PageNumberOmittingLevelRange = "2-5";

     // Ställ in en anpassad sträng som skiljer varje rubrik från dess sidnummer.
    field.EntrySeparator = "-";
    field.InsertHyperlinks = true;
    field.HideInWebLayout = false;
    field.PreserveLineBreaks = true;
    field.PreserveTabs = true;
    field.UseParagraphOutlineLevel = false;

    InsertNewPageWithHeading(builder, "First entry", "Heading 1");
    builder.Writeln("Paragraph text.");
    InsertNewPageWithHeading(builder, "Second entry", "Heading 1");
    InsertNewPageWithHeading(builder, "Third entry", "Quote");
    InsertNewPageWithHeading(builder, "Fourth entry", "Intense Quote");

    // Dessa två rubriker kommer att ha sidnumren utelämnade eftersom de ligger inom intervallet "2-5".
    InsertNewPageWithHeading(builder, "Fifth entry", "Heading 2");
    InsertNewPageWithHeading(builder, "Sixth entry", "Heading 3");

    // Den här posten visas inte eftersom "Rubrik 4" ligger utanför intervallet "1-3" som vi har ställt in tidigare.
    InsertNewPageWithHeading(builder, "Seventh entry", "Heading 4");

    builder.EndBookmark("MyBookmark");
    builder.Writeln("Paragraph text.");

    // Den här posten visas inte eftersom den ligger utanför bokmärket som anges av innehållsförteckningen.
    InsertNewPageWithHeading(builder, "Eighth entry", "Heading 1");

    Assert.AreEqual(" TOC  \\b MyBookmark \\t \"Quote; 6; Intense Quote; 7\" \\o 1-3 \\n 2-5 \\p - \\h \\x \\w", field.GetFieldCode());

    field.UpdatePageNumbers();
    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.TOC.docx");
}

/// <summary>
/// Starta en ny sida och infoga ett stycke av en angiven stil.
/// </summary>
public void InsertNewPageWithHeading(DocumentBuilder builder, string captionText, string styleName)
{
    builder.InsertBreak(BreakType.PageBreak);
    string originalStyle = builder.ParagraphFormat.StyleName;
    builder.ParagraphFormat.Style = builder.Document.Styles[styleName];
    builder.Writeln(captionText);
    builder.ParagraphFormat.Style = builder.Document.Styles[originalStyle];
}
```

### Se även

* class [FieldToc](../)
* namnutrymme [Aspose.Words.Fields](../../fieldtoc/)
* hopsättning [Aspose.Words](../../../)


