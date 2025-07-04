---
title: MailMerge.RegionStartTag
linktitle: RegionStartTag
articleTitle: RegionStartTag
second_title: Aspose.Words for .NET
description: Discover the MailMerge RegionStartTag property to easily define and customize mail merge regions, enhancing your document automation process.
type: docs
weight: 100
url: /net/aspose.words.mailmerging/mailmerge/regionstarttag/
---
## MailMerge.RegionStartTag property

Gets or sets a mail merge region start tag.

```csharp
public string RegionStartTag { get; set; }
```

## Examples

Shows how to create, list, and read mail merge regions.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// "TableStart" and "TableEnd" tags, which go inside MERGEFIELDs,
// denote the strings that signify the starts and ends of mail merge regions.
Assert.That(doc.MailMerge.RegionStartTag, Is.EqualTo("TableStart"));
Assert.That(doc.MailMerge.RegionEndTag, Is.EqualTo("TableEnd"));

// Use these tags to start and end a mail merge region named "MailMergeRegion1",
// which will contain MERGEFIELDs for two columns.
builder.InsertField(" MERGEFIELD TableStart:MailMergeRegion1");
builder.InsertField(" MERGEFIELD Column1");
builder.Write(", ");
builder.InsertField(" MERGEFIELD Column2");
builder.InsertField(" MERGEFIELD TableEnd:MailMergeRegion1");

// We can keep track of merge regions and their columns by looking at these collections.
IList<MailMergeRegionInfo> regions = doc.MailMerge.GetRegionsByName("MailMergeRegion1");

Assert.That(regions.Count, Is.EqualTo(1));
Assert.That(regions[0].Name, Is.EqualTo("MailMergeRegion1"));

string[] mergeFieldNames = doc.MailMerge.GetFieldNamesForRegion("MailMergeRegion1");

Assert.That(mergeFieldNames[0], Is.EqualTo("Column1"));
Assert.That(mergeFieldNames[1], Is.EqualTo("Column2"));

// Insert a region with the same name inside the existing region, which will make it a parent.
// Now a "Column2" field will be inside a new region.
builder.MoveToField(regions[0].Fields[1], false); 
builder.InsertField(" MERGEFIELD TableStart:MailMergeRegion1");
builder.MoveToField(regions[0].Fields[1], true);
builder.InsertField(" MERGEFIELD TableEnd:MailMergeRegion1");

// If we look up the name of duplicate regions using the "GetRegionsByName" method,
// it will return all such regions in a collection.
regions = doc.MailMerge.GetRegionsByName("MailMergeRegion1");

Assert.That(regions.Count, Is.EqualTo(2));
// Check that the second region now has a parent region.
Assert.That(regions[1].ParentRegion.Name, Is.EqualTo("MailMergeRegion1"));

mergeFieldNames = doc.MailMerge.GetFieldNamesForRegion("MailMergeRegion1", 1);

Assert.That(mergeFieldNames[0], Is.EqualTo("Column2"));
```

### See Also

* class [MailMerge](../)
* namespace [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* assembly [Aspose.Words](../../../)
