---
title: Aspose::Words::Saving::TxtSaveOptions::set_OfficeMathExportMode method
linktitle: set_OfficeMathExportMode
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::TxtSaveOptions::set_OfficeMathExportMode method. Specifies how OfficeMath will be written to the output file. Default value is Text in C++.'
type: docs
weight: 12500
url: /cpp/aspose.words.saving/txtsaveoptions/set_officemathexportmode/
---
## TxtSaveOptions::set_OfficeMathExportMode method


Specifies how OfficeMath will be written to the output file. Default value is [Text](../../txtofficemathexportmode/).

```cpp
void Aspose::Words::Saving::TxtSaveOptions::set_OfficeMathExportMode(Aspose::Words::Saving::TxtOfficeMathExportMode value)
```

## Examples


Shows how to export OfficeMath object as Latex in TXT.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(System::String(get_MyDir() + u"Office math.docx"));

auto saveOptions = System::MakeObject<Aspose::Words::Saving::TxtSaveOptions>();
saveOptions->set_OfficeMathExportMode(TxtOfficeMathExportMode::Latex);

doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.ExportOfficeMathAsLatexToText.txt", saveOptions);
```
## See Also

* Class [TxtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
