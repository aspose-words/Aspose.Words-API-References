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


Specifies how Aspose.Words exports [OfficeMath](../../aspose.words.math/officemath/) to [Text](../../aspose.words/saveformat/).

```cpp
enum class TxtOfficeMathExportMode : int
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Latex | 3 | Export [OfficeMath](../../aspose.words.math/officemath/) as LaTeX. |
| Text | 0 | Export [OfficeMath](../../aspose.words.math/officemath/) as plain text. |

## Examples


Shows how to export [OfficeMath](../../aspose.words.math/officemath/) object as Latex in TXT.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(System::String(get_MyDir() + u"Office math.docx"));

auto saveOptions = System::MakeObject<Aspose::Words::Saving::TxtSaveOptions>();
saveOptions->set_OfficeMathExportMode(TxtOfficeMathExportMode::Latex);

doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.ExportOfficeMathAsLatexToText.txt", saveOptions);
```
## See Also

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
