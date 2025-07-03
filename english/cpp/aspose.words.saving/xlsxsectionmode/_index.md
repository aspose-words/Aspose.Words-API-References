---
title: Aspose::Words::Saving::XlsxSectionMode enum
linktitle: XlsxSectionMode
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::XlsxSectionMode enum. Specifies how sections are handled when saving a document in the XLSX format in C++.'
type: docs
weight: 87000
url: /cpp/aspose.words.saving/xlsxsectionmode/
---
## XlsxSectionMode enum


Specifies how sections are handled when saving a document in the XLSX format.

```cpp
enum class XlsxSectionMode
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| MultipleWorksheets | 0 | Specifies that a separate worksheet is created for each section of a document. |
| SingleWorksheet | 1 | Specifies that all sections of a document are saved on one worksheet. |


## Examples



Shows how to save document as a separate worksheets. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");

// Each section of a document will be created as a separate worksheet.
// Use 'SingleWorksheet' to display all document on one worksheet.
auto xlsxSaveOptions = System::MakeObject<Aspose::Words::Saving::XlsxSaveOptions>();
xlsxSaveOptions->set_SectionMode(Aspose::Words::Saving::XlsxSectionMode::MultipleWorksheets);

doc->Save(get_ArtifactsDir() + u"XlsxSaveOptions.SelectionMode.xlsx", xlsxSaveOptions);
```

## See Also

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
