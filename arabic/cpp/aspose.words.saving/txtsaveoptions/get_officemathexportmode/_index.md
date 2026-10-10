---
title: "طريقة Aspose::Words::Saving::TxtSaveOptions::get_OfficeMathExportMode"
linktitle: "get_OfficeMathExportMode"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Saving::TxtSaveOptions::get_OfficeMathExportMode. تحدد كيفية كتابة OfficeMath إلى ملف الإخراج. القيمة الافتراضية هي Text في C++."
type: docs
weight: 5500
url: /ar/cpp/aspose.words.saving/txtsaveoptions/get_officemathexportmode/
---
## TxtSaveOptions::get_OfficeMathExportMode method


تحدد كيفية كتابة OfficeMath إلى ملف الإخراج. القيمة الافتراضية هي [Text](../../txtofficemathexportmode/).

```cpp
Aspose::Words::Saving::TxtOfficeMathExportMode Aspose::Words::Saving::TxtSaveOptions::get_OfficeMathExportMode() const
```


## أمثلة



يوضح كيفية تصدير كائن OfficeMath كـ Latex في TXT.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::TxtSaveOptions>();
saveOptions->set_OfficeMathExportMode(Aspose::Words::Saving::TxtOfficeMathExportMode::Latex);

doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.ExportOfficeMathAsLatexToText.txt", saveOptions);
```

## انظر أيضًا

* Enum [TxtOfficeMathExportMode](../../txtofficemathexportmode/)
* Class [TxtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
