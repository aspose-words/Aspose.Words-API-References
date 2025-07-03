---
title: Aspose::Words::Saving::XlsxSaveOptions::get_SectionMode method
linktitle: get_SectionMode
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::XlsxSaveOptions::get_SectionMode method. Gets or sets the way how sections are handled when saving to the output XLSX document. The default value is MultipleWorksheets in C++.'
type: docs
weight: 4500
url: /cpp/aspose.words.saving/xlsxsaveoptions/get_sectionmode/
---
## XlsxSaveOptions::get_SectionMode method


Gets or sets the way how sections are handled when saving to the output XLSX document. The default value is [MultipleWorksheets](../../xlsxsectionmode/).

```cpp
Aspose::Words::Saving::XlsxSectionMode Aspose::Words::Saving::XlsxSaveOptions::get_SectionMode() const
```


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

* Enum [XlsxSectionMode](../../xlsxsectionmode/)
* Class [XlsxSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
