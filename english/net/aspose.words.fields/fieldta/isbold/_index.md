---
title: "IsBold"
second_title: Aspose.Words for .NET API Reference
description: ""
type: docs
weight: 20
url: /net/aspose.words.fields/fieldta/isbold/
---
## FieldTA.IsBold property

Gets or sets whether to apply bold formatting to the page number for the entry.

```csharp
public bool IsBold { get; set; }
```

### Examples

Shows how to build and customize a table of authorities using TOA and TA fields.

```csharp
public void FieldTOA()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Insert a TOA field, which will create an entry for each TA field in the document,
    // displaying long citations and page numbers for each entry.
    FieldToa fieldToa = (FieldToa)builder.InsertField(FieldType.FieldTOA, false);

    // Set the entry category for our table. This TOA will now only include TA fields
    // that have a matching value in their EntryCategory property.
    fieldToa.EntryCategory = "1";

    // Moreover, the Table of Authorities category at index 1 is "Cases",
    // which will show up as our table's title if we set this variable to true.
    fieldToa.UseHeading = true;

    // We can further filter TA fields by naming a bookmark that they will need to be within the TOA bounds.
    fieldToa.BookmarkName = "MyBookmark";

    // By default, a dotted line page-wide tab appears between the TA field's citation
    // and its page number. We can replace it with any text we put on this property.
    // Inserting a tab character will preserve the original tab.
    fieldToa.EntrySeparator = " \t p.";

    // If we have multiple TA entries that share the same long citation,
    // all their respective page numbers will show up on one row.
    // We can use this property to specify a string that will separate their page numbers.
    fieldToa.PageNumberListSeparator = " & p. ";

    // We can set this to true to get our table to display the word "passim"
    // if there are five or more page numbers in one row.
    fieldToa.UsePassim = true;

    // One TA field can refer to a range of pages.
    // We can specify a string here to appear between the start and end page numbers for such ranges.
    fieldToa.PageRangeSeparator = " to ";

    // The format from the TA fields will carry over into our table.
    // We can disable this by setting the RemoveEntryFormatting flag.
    fieldToa.RemoveEntryFormatting = true;
    builder.Font.Color = Color.Green;
    builder.Font.Name = "Arial Black";

    Assert.AreEqual(" TOA  \\c 1 \\h \\b MyBookmark \\e \" \t p.\" \\l \" & p. \" \\p \\g \" to \" \\f", fieldToa.GetFieldCode());

    builder.InsertBreak(BreakType.PageBreak);

    // This TA field will not appear as an entry in the TOA since it is outside
    // the bookmark's bounds that the TOA's BookmarkName property specifies.
    FieldTA fieldTA = InsertToaEntry(builder, "1", "Source 1");

    Assert.AreEqual(" TA  \\c 1 \\l \"Source 1\"", fieldTA.GetFieldCode());

    // This TA field is inside the bookmark,
    // but the entry category does not match that of the table, so the TA field will not include it.
    builder.StartBookmark("MyBookmark");
    fieldTA = InsertToaEntry(builder, "2", "Source 2");

    // This entry will appear in the table.
    fieldTA = InsertToaEntry(builder, "1", "Source 3");

    // A TOA table does not display short citations,
    // but we can use them as a shorthand to refer to bulky source names that multiple TA fields reference.
    fieldTA.ShortCitation = "S.3";

    Assert.AreEqual(" TA  \\c 1 \\l \"Source 3\" \\s S.3", fieldTA.GetFieldCode());

    // We can format the page number to make it bold/italic using the following properties.
    // We will still see these effects if we set our table to ignore formatting.
    fieldTA = InsertToaEntry(builder, "1", "Source 2");
    fieldTA.IsBold = true;
    fieldTA.IsItalic = true;

    Assert.AreEqual(" TA  \\c 1 \\l \"Source 2\" \\b \\i", fieldTA.GetFieldCode());

    // We can configure TA fields to get their TOA entries to refer to a range of pages that a bookmark spans across.
    // Note that this entry refers to the same source as the one above to share one row in our table.
    // This row will have the page number of the entry above and the page range of this entry,
    // with the table's page list and page number range separators between page numbers.
    fieldTA = InsertToaEntry(builder, "1", "Source 3");
    fieldTA.PageRangeBookmarkName = "MyMultiPageBookmark";

    builder.StartBookmark("MyMultiPageBookmark");
    builder.InsertBreak(BreakType.PageBreak);
    builder.InsertBreak(BreakType.PageBreak);
    builder.InsertBreak(BreakType.PageBreak);
    builder.EndBookmark("MyMultiPageBookmark");

    Assert.AreEqual(" TA  \\c 1 \\l \"Source 3\" \\r MyMultiPageBookmark", fieldTA.GetFieldCode());

    // If we have enabled the "Passim" feature of our table, having 5 or more TA entries with the same source will invoke it.
    for (int i = 0; i < 5; i++)
    {
        InsertToaEntry(builder, "1", "Source 4");
    }

    builder.EndBookmark("MyBookmark");

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.TOA.TA.docx");
}

private static FieldTA InsertToaEntry(DocumentBuilder builder, string entryCategory, string longCitation)
{
    FieldTA field = (FieldTA)builder.InsertField(FieldType.FieldTOAEntry, false);
    field.EntryCategory = entryCategory;
    field.LongCitation = longCitation;

    builder.InsertBreak(BreakType.PageBreak);

    return field;
}
```

### See Also

* class [FieldTA](../../fieldta)
* namespace [Aspose.Words.Fields](../../fieldta)
* assembly [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
