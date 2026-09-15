---
title: "طريقة Aspose::Words::ImportFormatOptions::get_AppendDocumentWithNewPage"
linktitle: "get_AppendDocumentWithNewPage"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::ImportFormatOptions::get_AppendDocumentWithNewPage. يحصل على قيمة منطقية أو يضبطها تشير إلى ما إذا كان يجب تغيير نوع القسم المستورد الأول إلى NewPage بالقوة عند استدعاء AppendDocument(). القيمة الافتراضية هي true في C++."
type: docs
weight: 3500
url: /ar/cpp/aspose.words/importformatoptions/get_appenddocumentwithnewpage/
---
## ImportFormatOptions::get_AppendDocumentWithNewPage method


يحصل على أو يضبط قيمة منطقية تشير إلى ما إذا كان يجب تغيير نوع القسم المستورد الأول إلى [NewPage](../../sectionstart/) بالقوة عند استدعاء [AppendDocument()](../). القيمة الافتراضية هي **true**.

```cpp
bool Aspose::Words::ImportFormatOptions::get_AppendDocumentWithNewPage() const
```


## أمثلة



يعرض كيفية الحفاظ على نوع القسم الأصلي.
```cpp
auto dstDoc = System::MakeObject<Aspose::Words::Document>();
auto srcDoc = System::MakeObject<Aspose::Words::Document>();

srcDoc->get_FirstSection()->get_PageSetup()->set_SectionStart(Aspose::Words::SectionStart::Continuous);

auto options = System::MakeObject<Aspose::Words::ImportFormatOptions>();
options->set_AppendDocumentWithNewPage(false);
dstDoc->AppendDocument(srcDoc, Aspose::Words::ImportFormatMode::KeepSourceFormatting, options);

ASSERT_EQ(Aspose::Words::SectionStart::Continuous, dstDoc->get_Sections()->idx_get(1)->get_PageSetup()->get_SectionStart());
```

## انظر أيضًا

* Class [ImportFormatOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
