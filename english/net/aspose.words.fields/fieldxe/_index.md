---
title: FieldXE
second_title: Aspose.Words for .NET API Reference
description: 
type: docs
weight: 2410
url: /net/aspose.words.fields/fieldxe/
---
## FieldXE class

Implements the XE field.

```csharp
public class FieldXE : Field
```

## Constructors

| Name | Description |
| --- | --- |
| [FieldXE](fieldxe)() | The default constructor. |

## Properties

| Name | Description |
| --- | --- |
| [EntryType](entrytype) { get; set; } | Gets or sets an index entry type. |
| [IsBold](isbold) { get; set; } | Gets or sets whether to apply bold formatting to the entry's page number. |
| [IsItalic](isitalic) { get; set; } | Gets or sets whether to apply italic formatting to the entry's page number. |
| [PageNumberReplacement](pagenumberreplacement) { get; set; } | Gets or sets text used in place of a page number. |
| [PageRangeBookmarkName](pagerangebookmarkname) { get; set; } | Gets or sets the name of the bookmark that marks a range of pages that is inserted as the entry's page number. |
| [Text](text) { get; set; } | Gets or sets the text of the entry. |
| [Yomi](yomi) { get; set; } | Gets or sets the yomi (first phonetic character for sorting indexes) for the index entry |

### Remarks

Defines the text and page number for an index entry, which is used by an INDEX field.

### Examples

Shows how to create an INDEX field, and then use XE fields to populate it with entries.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Create an INDEX field which will display an entry for each XE field found in the document.
// Each entry will display the XE field's Text property value on the left side
// and the page containing the XE field on the right.
// If the XE fields have the same value in their "Text" property,
// the INDEX field will group them into one entry.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);

// Configure the INDEX field only to display XE fields that are within the bounds
// of a bookmark named "MainBookmark", and whose "EntryType" properties have a value of "A".
// For both INDEX and XE fields, the "EntryType" property only uses the first character of its string value.
index.BookmarkName = "MainBookmark";
index.EntryType = "A";

Assert.AreEqual(" INDEX  \\b MainBookmark \\f A", index.GetFieldCode());

// On a new page, start the bookmark with a name that matches the value
// of the INDEX field's "BookmarkName" property.
builder.InsertBreak(BreakType.PageBreak);
builder.StartBookmark("MainBookmark");

// The INDEX field will pick up this entry because it is inside the bookmark,
// and its entry type also matches the INDEX field's entry type.
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Index entry 1";
indexEntry.EntryType = "A";

Assert.AreEqual(" XE  \"Index entry 1\" \\f A", indexEntry.GetFieldCode());

// Insert an XE field that will not appear in the INDEX because the entry types do not match.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Index entry 2";
indexEntry.EntryType = "B";

// End the bookmark and insert an XE field afterwards.
// It is of the same type as the INDEX field, but will not appear
// since it is outside the bookmark's boundaries.
builder.EndBookmark("MainBookmark");
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Index entry 3";
indexEntry.EntryType = "A";

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.Filtering.docx");
```

Shows how to populate an INDEX field with entries using XE fields, and also modify its appearance.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Create an INDEX field which will display an entry for each XE field found in the document.
// Each entry will display the XE field's Text property value on the left side,
// and the number of the page that contains the XE field on the right.
// If the XE fields have the same value in their "Text" property,
// the INDEX field will group them into one entry.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);
index.LanguageId = "1033";

// Setting this property's value to "A" will group all the entries by their first letter,
// and place that letter in uppercase above each group.
index.Heading = "A";

// Set the table created by the INDEX field to span over 2 columns.
index.NumberOfColumns = "2";

// Set any entries with starting letters outside the "a-c" character range to be omitted.
index.LetterRange = "a-c";

Assert.AreEqual(" INDEX  \\z 1033 \\h A \\c 2 \\p a-c", index.GetFieldCode());

// These next two XE fields will show up under the "A" heading,
// with their respective text stylings also applied to their page numbers.
builder.InsertBreak(BreakType.PageBreak);
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Apple";
indexEntry.IsItalic = true;

Assert.AreEqual(" XE  Apple \\i", indexEntry.GetFieldCode());

builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Apricot";
indexEntry.IsBold = true;

Assert.AreEqual(" XE  Apricot \\b", indexEntry.GetFieldCode());

// Both the next two XE fields will be under a "B" and "C" heading in the INDEX fields table of contents.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Banana";

builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Cherry";

// INDEX fields sort all entries alphabetically, so this entry will show up under "A" with the other two.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Avocado";

// This entry will not appear because it starts with the letter "D",
// which is outside the "a-c" character range that the INDEX field's LetterRange property defines.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Durian";

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.Formatting.docx");
```

### See Also

* class [Field](../field)
* namespace [Aspose.Words.Fields](../../aspose.words.fields)
* assembly [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
