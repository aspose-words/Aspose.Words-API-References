---
title: "Aspose::Words::Saving::TxtOfficeMathExportMode enum"
linktitle: "TxtOfficeMathExportMode"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Saving::TxtOfficeMathExportMode enum. يحدد كيفية تصدير Aspose.Words لـ OfficeMath إلى نص في C++."
type: docs
weight: 86250
url: /ar/cpp/aspose.words.saving/txtofficemathexportmode/
---
## TxtOfficeMathExportMode enum


يحدد كيفية تصدير Aspose.Words لـ OfficeMath إلى [Text](../../aspose.words/saveformat/).

```cpp
enum class TxtOfficeMathExportMode
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| Text | 0 | تصدير OfficeMath كنص عادي. |
| Latex | 3 | تصدير OfficeMath كـ LaTeX. |


## أمثلة



يوضح كيفية تصدير كائن OfficeMath كـ Latex في TXT.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::TxtSaveOptions>();
saveOptions->set_OfficeMathExportMode(Aspose::Words::Saving::TxtOfficeMathExportMode::Latex);

doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.ExportOfficeMathAsLatexToText.txt", saveOptions);
```

## انظر أيضًا

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
