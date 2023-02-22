---
title: RegionEndTag
second_title: Aspose.Words for .NET API Reference
description: MailMerge property. Gets or sets a mail merge region end tag in C#.
type: docs
weight: 90
url: /net/aspose.words.mailmerging/mailmerge/regionendtag/
---
## MailMerge.RegionEndTag property

Gets or sets a mail merge region end tag.

```csharp
public string RegionEndTag { get; set; }
```

## Examples

Shows how to create, list, and read mail merge regions.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// "TableStart" and "TableEnd" tags, which go inside MERGEFIELDs,
// denote the strings that signify the starts and ends of mail merge regions.
Assert.AreEqual("TableStart", doc.MailMerge.RegionStartTag);
Assert.AreEqual("TableEnd", doc.MailMerge.RegionEndTag);

// Use these tags to start and end a mail merge region named "MailMergeRegion1",
// which will contain MERGEFIELDs for two columns.
builder.InsertField(" MERGEFIELD TableStart:MailMergeRegion1");
builder.InsertField(" MERGEFIELD Column1");
builder.Write(", ");
builder.InsertField(" MERGEFIELD Column2");
builder.InsertField(" MERGEFIELD TableEnd:MailMergeRegion1");

// We can keep track of merge regions and their columns by looking at these collections.
IList<MailMergeRegionInfo> regions = doc.MailMerge.GetRegionsByName("MailMergeRegion1");

Assert.AreEqual(1, regions.Count);
Assert.AreEqual("MailMergeRegion1", regions[0].Name);

string[] mergeFieldNames = doc.MailMerge.GetFieldNamesForRegion("MailMergeRegion1");

Assert.AreEqual("Column1", mergeFieldNames[0]);
Assert.AreEqual("Column2", mergeFieldNames[1]);

// Insert a region with the same name inside the existing region, which will make it a parent.
// Now a "Column2" field will be inside a new region.
builder.MoveToField(regions[0].Fields[1], false); 
builder.InsertField(" MERGEFIELD TableStart:MailMergeRegion1");
builder.MoveToField(regions[0].Fields[1], true);
builder.InsertField(" MERGEFIELD TableEnd:MailMergeRegion1");

// If we look up the name of duplicate regions using the "GetRegionsByName" method,
// it will return all such regions in a collection.
regions = doc.MailMerge.GetRegionsByName("MailMergeRegion1");

Assert.AreEqual(2, regions.Count);
// Check that the second region now has a parent region.
Assert.AreEqual("MailMergeRegion1", regions[1].ParentRegion.Name);

mergeFieldNames = doc.MailMerge.GetFieldNamesForRegion("MailMergeRegion1", 1);

Assert.AreEqual("Column2", mergeFieldNames[0]);
```

### See Also

* class [MailMerge](../)
* namespace [Aspose.Words.MailMerging](../../mailmerge/)
* assembly [Aspose.Words](../../../)
