---
title: "تعداد Aspose::Words::Saving::XlsxSectionMode"
linktitle: "XxlsxSectionMode"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "تعداد Aspose::Words::Saving::XlsxSectionMode. يحدد كيفية معالجة الأقسام عند حفظ مستند بتنسيق XLSX في C++."
type: docs
weight: 87000
url: /ar/cpp/aspose.words.saving/xlsxsectionmode/
---
## XlsxSectionMode enum


يحدد كيفية معالجة الأقسام عند حفظ المستند بتنسيق XLSX.

```cpp
enum class XlsxSectionMode
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| MultipleWorksheets | 0 | يحدد أنه يتم إنشاء ورقة عمل منفصلة لكل قسم من المستند. |
| SingleWorksheet | 1 | يحدد أنه يتم حفظ جميع أقسام المستند في ورقة عمل واحدة. |


## أمثلة



يوضح كيفية حفظ المستند كأوراق عمل منفصلة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");

// سيتم إنشاء كل قسم من المستند كورقة عمل منفصلة.
// استخدم 'SingleWorksheet' لعرض جميع المستند في ورقة عمل واحدة.
auto xlsxSaveOptions = System::MakeObject<Aspose::Words::Saving::XlsxSaveOptions>();
xlsxSaveOptions->set_SectionMode(Aspose::Words::Saving::XlsxSectionMode::MultipleWorksheets);

doc->Save(get_ArtifactsDir() + u"XlsxSaveOptions.SelectionMode.xlsx", xlsxSaveOptions);
```

## انظر أيضًا

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
