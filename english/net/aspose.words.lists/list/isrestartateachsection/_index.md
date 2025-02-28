---
title: List.IsRestartAtEachSection
linktitle: IsRestartAtEachSection
articleTitle: IsRestartAtEachSection
second_title: Aspose.Words for .NET
description: Discover the IsRestartAtEachSection property to control list numbering in sections. Enhance document organization with this easy-to-use feature!
type: docs
weight: 50
url: /net/aspose.words.lists/list/isrestartateachsection/
---
## List.IsRestartAtEachSection property

Specifies whether list should be restarted at each section. Default value is `false`.

```csharp
public bool IsRestartAtEachSection { get; set; }
```

## Remarks

This option is supported only in RTF, DOC and DOCX document formats.

This option will be written to DOCX only if [`OoxmlCompliance`](../../../aspose.words.saving/ooxmlcompliance/) is higher then Ecma376_2006.

## Examples

Shows how to configure a list to restart numbering at each section.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

doc.Lists.Add(ListTemplate.NumberDefault);

Aspose.Words.Lists.List list = doc.Lists[0];
list.IsRestartAtEachSection = restartListAtEachSection;

// The "IsRestartAtEachSection" property will only be applicable when
// the document's OOXML compliance level is to a standard that is newer than "OoxmlComplianceCore.Ecma376".
OoxmlSaveOptions options = new OoxmlSaveOptions
{
    Compliance = OoxmlCompliance.Iso29500_2008_Transitional
};

builder.ListFormat.List = list;

builder.Writeln("List item 1");
builder.Writeln("List item 2");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Writeln("List item 3");
builder.Writeln("List item 4");

doc.Save(ArtifactsDir + "OoxmlSaveOptions.RestartingDocumentList.docx", options);

doc = new Document(ArtifactsDir + "OoxmlSaveOptions.RestartingDocumentList.docx");

Assert.AreEqual(restartListAtEachSection, doc.Lists[0].IsRestartAtEachSection);
```

### See Also

* class [List](../)
* namespace [Aspose.Words.Lists](../../../aspose.words.lists/)
* assembly [Aspose.Words](../../../)
