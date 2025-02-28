---
title: FieldIndex.RunSubentriesOnSameLine
linktitle: RunSubentriesOnSameLine
articleTitle: RunSubentriesOnSameLine
second_title: Aspose.Words for .NET
description: Discover the FieldIndex RunSubentriesOnSameLine property to easily manage subentries inline with main entries for streamlined data organization.
type: docs
weight: 140
url: /net/aspose.words.fields/fieldindex/runsubentriesonsameline/
---
## FieldIndex.RunSubentriesOnSameLine property

Gets or sets whether run subentries into the same line as the main entry.

```csharp
public bool RunSubentriesOnSameLine { get; set; }
```

## Examples

Shows how to work with subentries in an INDEX field.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Create an INDEX field which will display an entry for each XE field found in the document.
// Each entry will display the XE field's Text property value on the left side,
// and the number of the page that contains the XE field on the right.
// The INDEX entry will collect all XE fields with matching values in the "Text" property
// into one entry as opposed to making an entry for each XE field.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);
index.PageNumberSeparator = ", see page ";
index.Heading = "A";

// XE fields that have a Text property whose value becomes the heading of the INDEX entry.
// If this value contains two string segments split by a colon (the INDEX entry will treat :) delimiter,
// the first segment is heading, and the second segment will become the subheading.
// The INDEX field first groups entries alphabetically, then, if there are multiple XE fields with the same
// headings, the INDEX field will further subgroup them by the values of these headings.
// There can be multiple subgrouping layers, depending on how many times
// the Text properties of XE fields get segmented like this.
// By default, an INDEX field entry group will create a new line for every subheading within this group. 
// We can set the RunSubentriesOnSameLine flag to true to keep the heading,
// and every subheading for the group on one line instead, which will make the INDEX field more compact.
index.RunSubentriesOnSameLine = runSubentriesOnTheSameLine;

if (runSubentriesOnTheSameLine)
    Assert.AreEqual(" INDEX  \\e \", see page \" \\h A \\r", index.GetFieldCode());
else
    Assert.AreEqual(" INDEX  \\e \", see page \" \\h A", index.GetFieldCode());

// Insert two XE fields, each on a new page, and with the same heading named "Heading 1",
// which the INDEX field will use to group them.
// If RunSubentriesOnSameLine is false, then the INDEX table will create three lines:
// one line for the grouping heading "Heading 1", and one more line for each subheading.
// If RunSubentriesOnSameLine is true, then the INDEX table will create a one-line
// entry that encompasses the heading and every subheading.
builder.InsertBreak(BreakType.PageBreak);
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Heading 1:Subheading 1";

Assert.AreEqual(" XE  \"Heading 1:Subheading 1\"", indexEntry.GetFieldCode());

builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Heading 1:Subheading 2";

doc.UpdatePageLayout();
doc.UpdateFields();
doc.Save(ArtifactsDir + $"Field.INDEX.XE.Subheading.docx");
```

### See Also

* class [FieldIndex](../)
* namespace [Aspose.Words.Fields](../../../aspose.words.fields/)
* assembly [Aspose.Words](../../../)
