---
title: FieldIndex
second_title: Aspose.Words for .NET API Reference
description: 
type: docs
weight: 1870
url: /net/aspose.words.fields/fieldindex/
---
## FieldIndex class

Implements the INDEX field.

```csharp
public class FieldIndex : Field
```

## Constructors

| Name | Description |
| --- | --- |
| [FieldIndex](fieldindex)() | The default constructor. |

## Properties

| Name | Description |
| --- | --- |
| [BookmarkName](../../aspose.words.fields/fieldindex/bookmarkname) { get; set; } | Gets or sets the name of the bookmark that marks the portion of the document used to build the index. |
| [CrossReferenceSeparator](../../aspose.words.fields/fieldindex/crossreferenceseparator) { get; set; } | Gets or sets the character sequence that is used to separate cross references and other entries. |
| [DisplayResult](../../aspose.words.fields/field/displayresult) { get; } | Gets the text that represents the displayed field result. |
| [End](../../aspose.words.fields/field/end) { get; } | Gets the node that represents the field end. |
| [EntryType](../../aspose.words.fields/fieldindex/entrytype) { get; set; } | Gets or sets an index entry type used to build the index. |
| [Format](../../aspose.words.fields/field/format) { get; } | Gets a [`FieldFormat`](../fieldformat) object that provides typed access to field's formatting. |
| [HasPageNumberSeparator](../../aspose.words.fields/fieldindex/haspagenumberseparator) { get; } | Gets a value indicating whether a page number separator is overridden through the field's code. |
| [HasSequenceName](../../aspose.words.fields/fieldindex/hassequencename) { get; } | Gets a value indicating whether a sequence should be used while the field's result building. |
| [Heading](../../aspose.words.fields/fieldindex/heading) { get; set; } | Gets or sets a heading that appears at the start of each set of entries for any given letter. |
| [IsDirty](../../aspose.words.fields/field/isdirty) { get; set; } | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [IsLocked](../../aspose.words.fields/field/islocked) { get; set; } | Gets or sets whether the field is locked (should not recalculate its result). |
| [LanguageId](../../aspose.words.fields/fieldindex/languageid) { get; set; } | Gets or sets the language ID used to generate the index. |
| [LetterRange](../../aspose.words.fields/fieldindex/letterrange) { get; set; } | Gets or sets a range of letters to which limit the index. |
| [LocaleId](../../aspose.words.fields/field/localeid) { get; set; } | Gets or sets the LCID of the field. |
| [NumberOfColumns](../../aspose.words.fields/fieldindex/numberofcolumns) { get; set; } | Gets or sets the number of columns per page used when building the index. |
| [PageNumberListSeparator](../../aspose.words.fields/fieldindex/pagenumberlistseparator) { get; set; } | Gets or sets the character sequence that is used to separate two page numbers in a page number list. |
| [PageNumberSeparator](../../aspose.words.fields/fieldindex/pagenumberseparator) { get; set; } | Gets or sets the character sequence that is used to separate an index entry and its page number. |
| [PageRangeSeparator](../../aspose.words.fields/fieldindex/pagerangeseparator) { get; set; } | Gets or sets the character sequence that is used to separate the start and end of a page range. |
| [Result](../../aspose.words.fields/field/result) { get; set; } | Gets or sets text that is between the field separator and field end. |
| [RunSubentriesOnSameLine](../../aspose.words.fields/fieldindex/runsubentriesonsameline) { get; set; } | Gets or sets whether run subentries into the same line as the main entry. |
| [Separator](../../aspose.words.fields/field/separator) { get; } | Gets the node that represents the field separator. Can be null. |
| [SequenceName](../../aspose.words.fields/fieldindex/sequencename) { get; set; } | Gets or sets the name of a sequence whose number is included with the page number. |
| [SequenceSeparator](../../aspose.words.fields/fieldindex/sequenceseparator) { get; set; } | Gets or sets the character sequence that is used to separate sequence numbers and page numbers. |
| [Start](../../aspose.words.fields/field/start) { get; } | Gets the node that represents the start of the field. |
| virtual [Type](../../aspose.words.fields/field/type) { get; } | Gets the Microsoft Word field type. |
| [UseYomi](../../aspose.words.fields/fieldindex/useyomi) { get; set; } | Gets or sets whether to enable the use of yomi text for index entries. |

## Methods

| Name | Description |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)() | Returns text between field start and field separator (or field end if there is no separator). Both field code and field result of child fields are included. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)(bool) | Returns text between field start and field separator (or field end if there is no separator). |
| [Remove](../../aspose.words.fields/field/remove)() | Removes the field from the document. Returns a node right after the field. If the field's end is the last child of its parent node, returns its parent paragraph. If the field is already removed, returns **null**. |
| [Unlink](../../aspose.words.fields/field/unlink)() | Performs the field unlink. |
| [Update](../../aspose.words.fields/field/update)() | Performs the field update. Throws if the field is being updated already. |
| [Update](../../aspose.words.fields/field/update)(bool) | Performs a field update. Throws if the field is being updated already. |

## Remarks

Builds an index using the index entries specified by XE fields, and inserts that index at this place in the document.

## Examples

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
