---
title: FieldOptions.CustomTocStyleSeparator
linktitle: CustomTocStyleSeparator
articleTitle: CustomTocStyleSeparator
second_title: Aspose.Words för .NET
description: Upptäck egenskapen FieldOptions CustomTocStyleSeparator för att enkelt anpassa ditt FieldToc-fälts stilavgränsare för förbättrad dokumentnavigering.
type: docs
weight: 60
url: /sv/net/aspose.words.fields/fieldoptions/customtocstyleseparator/
---
## FieldOptions.CustomTocStyleSeparator property

Hämtar eller ställer in anpassad stilavgränsare för \t-växeln i[`FieldToc`](../../fieldtoc/) fält.

```csharp
public string CustomTocStyleSeparator { get; set; }
```

## Anmärkningar

Som standard är anpassade stilar definierade av \t-växeln i[`FieldToc`](../../fieldtoc/) fält är separerade med ett avgränsare taget från den aktuella kulturen. Den här egenskapen åsidosätter det beteendet genom att ange ett användardefinierat avgränsare.

## Exempel

Visar hur man infogar en innehållsförteckning och fyller den med poster baserat på rubrikformat.

```csharp
public void FieldToc()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.StartBookmark("MyBookmark");

    // Infoga ett innehållsförteckningsfält, vilket sammanställer alla rubriker till en innehållsförteckning.
    // För varje rubrik skapar det här fältet en rad med texten i den rubrikstilen till vänster,
    // och sidan där rubriken visas till höger.
    FieldToc field = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

    // Använd egenskapen BookmarkName för att endast lista rubriker
    // som visas inom gränserna för ett bokmärke med namnet "MittBokmärke".
    field.BookmarkName = "MyBookmark";

    // Text med en inbyggd rubrikstil, till exempel "Rubrik 1", räknas som en rubrik.
    // Vi kan namnge ytterligare stilar som ska hämtas som rubriker av innehållsförteckningen i den här egenskapen och deras innehållsförteckningsnivåer.
    field.CustomStyles = "Quote; 6; Intense Quote; 7";

    // Som standard separeras nivåerna för stilar/innehållsförteckningar i egenskapen CustomStyles med ett kommatecken,
    // men vi kan ställa in en anpassad avgränsare i den här egenskapen.
    doc.FieldOptions.CustomTocStyleSeparator = ";";

    // Konfigurera fältet för att exkludera rubriker som har innehållsförteckningsnivåer utanför detta intervall.
    field.HeadingLevelRange = "1-3";

    // Innehållsförteckningen visar inte sidnumren för rubriker vars innehållsförteckningsnivåer ligger inom detta intervall.
    field.PageNumberOmittingLevelRange = "2-5";

     // Ställ in en anpassad sträng som separerar varje rubrik från dess sidnummer.
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

    // Den här posten visas inte eftersom "Rubrik 4" ligger utanför intervallet "1-3" som vi ställde in tidigare.
    InsertNewPageWithHeading(builder, "Seventh entry", "Heading 4");

    builder.EndBookmark("MyBookmark");
    builder.Writeln("Paragraph text.");

    // Den här posten visas inte eftersom den ligger utanför bokmärket som anges i innehållsförteckningen.
    InsertNewPageWithHeading(builder, "Eighth entry", "Heading 1");

    Assert.AreEqual(" TOC  \\b MyBookmark \\t \"Quote; 6; Intense Quote; 7\" \\o 1-3 \\n 2-5 \\p - \\h \\x \\w", field.GetFieldCode());

    field.UpdatePageNumbers();
    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.TOC.docx");
}

/// <summary>
/// Börja en ny sida och infoga ett stycke med en angiven stil.
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

* class [FieldOptions](../)
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)
