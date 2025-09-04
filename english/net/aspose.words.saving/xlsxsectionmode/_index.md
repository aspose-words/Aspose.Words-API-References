---
title: XlsxSectionMode Enum
linktitle: XlsxSectionMode
articleTitle: XlsxSectionMode
second_title: Aspose.Words for .NET
description: Discover how the Aspose.Words XlsxSectionMode enum optimizes document saving in XLSX format, enhancing your workflow and document management.
type: docs
weight: 6570
url: /net/aspose.words.saving/xlsxsectionmode/
---
## XlsxSectionMode enumeration

Specifies how sections are handled when saving a document in the XLSX format.

```csharp
public enum XlsxSectionMode
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| MultipleWorksheets | `0` | Specifies that a separate worksheet is created for each section of a document. |
| SingleWorksheet | `1` | Specifies that all sections of a document are saved on one worksheet. |

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

* namespace [Aspose.Words.Saving](../../aspose.words.saving/)
* assembly [Aspose.Words](../../)
