---
title: Aspose::Words::Saving::TxtOfficeMathExportMode enum
linktitle: TxtOfficeMathExportMode
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::TxtOfficeMathExportMode enum. Specifies how Aspose.Words exports OfficeMath to Text in C++.'
type: docs
weight: 86250
url: /cpp/aspose.words.saving/txtofficemathexportmode/
---
## TxtOfficeMathExportMode enum


Specifies how Aspose.Words exports OfficeMath to [Text](../../aspose.words/saveformat/).

```cpp
enum class TxtOfficeMathExportMode
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Text | 0 | Export OfficeMath as plain text. |
| Latex | 3 | Export OfficeMath as LaTeX. |


## Examples



Shows how to export OfficeMath object as Latex in TXT. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::TxtSaveOptions>();
saveOptions->set_OfficeMathExportMode(Aspose::Words::Saving::TxtOfficeMathExportMode::Latex);

doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.ExportOfficeMathAsLatexToText.txt", saveOptions);
```

## See Also

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
