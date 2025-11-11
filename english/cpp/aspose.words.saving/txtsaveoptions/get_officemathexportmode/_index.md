---
title: Aspose::Words::Saving::TxtSaveOptions::get_OfficeMathExportMode method
linktitle: get_OfficeMathExportMode
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::TxtSaveOptions::get_OfficeMathExportMode method. Specifies how OfficeMath will be written to the output file. Default value is Text in C++.'
type: docs
weight: 5500
url: /cpp/aspose.words.saving/txtsaveoptions/get_officemathexportmode/
---
## TxtSaveOptions::get_OfficeMathExportMode method


Specifies how OfficeMath will be written to the output file. Default value is [Text](../../txtofficemathexportmode/).

```cpp
Aspose::Words::Saving::TxtOfficeMathExportMode Aspose::Words::Saving::TxtSaveOptions::get_OfficeMathExportMode() const
```


## Examples



Shows how to export OfficeMath object as Latex in TXT. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::TxtSaveOptions>();
saveOptions->set_OfficeMathExportMode(Aspose::Words::Saving::TxtOfficeMathExportMode::Latex);

doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.ExportOfficeMathAsLatexToText.txt", saveOptions);
```

## See Also

* Enum [TxtOfficeMathExportMode](../../txtofficemathexportmode/)
* Class [TxtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
