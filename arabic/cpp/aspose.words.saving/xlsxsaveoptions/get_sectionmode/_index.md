---
title: "طريقة Aspose::Words::Saving::XlsxSaveOptions::get_SectionMode"
linktitle: "get_SectionMode"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Saving::XlsxSaveOptions::get_SectionMode method. يحصل أو يحدد الطريقة التي يتم بها معالجة الأقسام عند الحفظ إلى مستند XLSX الناتج. القيمة الافتراضية هي MultipleWorksheets في C++."
type: docs
weight: 4500
url: /ar/cpp/aspose.words.saving/xlsxsaveoptions/get_sectionmode/
---
## XlsxSaveOptions::get_SectionMode method


يحصل أو يحدد الطريقة التي يتم بها معالجة الأقسام عند الحفظ إلى مستند XLSX الناتج. القيمة الافتراضية هي [MultipleWorksheets](../../xlsxsectionmode/).

```cpp
Aspose::Words::Saving::XlsxSectionMode Aspose::Words::Saving::XlsxSaveOptions::get_SectionMode() const
```


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

* Enum [XlsxSectionMode](../../xlsxsectionmode/)
* Class [XlsxSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
