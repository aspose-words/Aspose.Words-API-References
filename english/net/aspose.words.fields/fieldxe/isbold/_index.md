---
title: FieldXE.IsBold
linktitle: IsBold
articleTitle: IsBold
second_title: Aspose.Words for .NET
description: Enhance your FieldXE experience! Control bold formatting for entry page numbers effortlessly with the IsBold property. Boost readability and style!
type: docs
weight: 30
url: /net/aspose.words.fields/fieldxe/isbold/
---
## FieldXE.IsBold property

Gets or sets whether to apply bold formatting to the entry's page number.

```csharp
public bool IsBold { get; set; }
```

## Examples

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

Assert.That(index.GetFieldCode(), Is.EqualTo(" INDEX  \\z 1033 \\h A \\c 2 \\p a-c"));

// These next two XE fields will show up under the "A" heading,
// with their respective text stylings also applied to their page numbers.
builder.InsertBreak(BreakType.PageBreak);
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Apple";
indexEntry.IsItalic = true;

Assert.That(indexEntry.GetFieldCode(), Is.EqualTo(" XE  Apple \\i"));

builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Apricot";
indexEntry.IsBold = true;

Assert.That(indexEntry.GetFieldCode(), Is.EqualTo(" XE  Apricot \\b"));

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

doc.UpdatePageLayout();
doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.Formatting.docx");
```

### See Also

* class [FieldXE](../)
* namespace [Aspose.Words.Fields](../../../aspose.words.fields/)
* assembly [Aspose.Words](../../../)
