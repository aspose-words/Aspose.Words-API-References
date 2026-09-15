---
title: "Aspose::Words::ImportFormatOptions::get_IgnoreHeaderFooter method"
linktitle: "get_IgnoreHeaderFooter"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::ImportFormatOptions::get_IgnoreHeaderFooter method. يحصل على أو يضبط قيمة منطقية تحدد أن تنسيق المحتوى في رؤوس/تذييلات المصدر يتم تجاهله إذا تم استخدام وضع KeepSourceFormatting. القيمة الافتراضية هي true في C++."
type: docs
weight: 5000
url: /ar/cpp/aspose.words/importformatoptions/get_ignoreheaderfooter/
---
## ImportFormatOptions::get_IgnoreHeaderFooter method


يحصل على أو يضبط قيمة منطقية تحدد أن تنسيق المحتوى في رؤوس/تذييلات المصدر يتم تجاهله إذا تم استخدام وضع [KeepSourceFormatting](../../importformatmode/). القيمة الافتراضية هي **true**.

```cpp
bool Aspose::Words::ImportFormatOptions::get_IgnoreHeaderFooter() const
```


## أمثلة



يعرض كيفية تحديد تجاهل أو عدم تجاهل تنسيق المحتوى في رؤوس/تذييلات المصدر.
```cpp
auto dstDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");
auto srcDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Header and footer types.docx");

// إذا كان 'IgnoreHeaderFooter' هو false فإن التنسيق الأصلي لمحتوى الرأس/التذييل
// سيتم استخدام "Header and footer types.docx".
// إذا كان 'IgnoreHeaderFooter' صحيحًا فإن تنسيق محتوى الرأس/التذييل
// سيتم استخدام "Document.docx".
auto importFormatOptions = System::MakeObject<Aspose::Words::ImportFormatOptions>();
importFormatOptions->set_IgnoreHeaderFooter(false);

dstDoc->AppendDocument(srcDoc, Aspose::Words::ImportFormatMode::KeepSourceFormatting, importFormatOptions);

dstDoc->Save(get_ArtifactsDir() + u"DocumentBuilder.DoNotIgnoreHeaderFooter.docx");
```

## انظر أيضًا

* Class [ImportFormatOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
