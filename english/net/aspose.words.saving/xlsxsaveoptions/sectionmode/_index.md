---
title: XlsxSaveOptions.SectionMode
linktitle: SectionMode
articleTitle: SectionMode
second_title: Aspose.Words for .NET
description: XlsxSaveOptions SectionMode property. Gets or sets the way how sections are handled when saving to the output XLSX document. The default value is MultipleWorksheets in C#.
type: docs
weight: 50
url: /net/aspose.words.saving/xlsxsaveoptions/sectionmode/
---
## XlsxSaveOptions.SectionMode property

Gets or sets the way how sections are handled when saving to the output XLSX document. The default value is MultipleWorksheets.

```csharp
public XlsxSectionMode SectionMode { get; set; }
```

## Examples

Shows how to save document as a separate worksheets.

```csharp
Document doc = new Document(MyDir + "Big document.docx");

// Each section of a document will be created as a separate worksheet.
// Use 'SingleWorksheet' to display all document on one worksheet.
XlsxSaveOptions xlsxSaveOptions = new XlsxSaveOptions();
xlsxSaveOptions.SectionMode = XlsxSectionMode.MultipleWorksheets;

doc.Save(ArtifactsDir + "XlsxSaveOptions.SelectionMode.xlsx", xlsxSaveOptions);
```

### See Also

* enum [XlsxSectionMode](../../xlsxsectionmode/)
* class [XlsxSaveOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
