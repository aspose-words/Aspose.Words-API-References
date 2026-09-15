---
title: "طريقة Aspose::Words::PageSetup::get_DifferentFirstPageHeaderFooter"
linktitle: "get_DifferentFirstPageHeaderFooter"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::PageSetup::get_DifferentFirstPageHeaderFooter. صحيحة إذا تم استخدام رأس أو تذييل مختلف في الصفحة الأولى في C++."
type: docs
weight: 13000
url: /ar/cpp/aspose.words/pagesetup/get_differentfirstpageheaderfooter/
---
## PageSetup::get_DifferentFirstPageHeaderFooter method


صحيح إذا تم استخدام رأس أو تذييل مختلف في الصفحة الأولى.

```cpp
bool Aspose::Words::PageSetup::get_DifferentFirstPageHeaderFooter()
```


## أمثلة



يظهر كيفية تمكين أو تعطيل رؤوس/تذييلات أساسية.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// فيما يلي نوعان من الرؤوس/التذييلات.
// 1 -  رأس/تذييل "First"، الذي يظهر في الصفحة الأولى من القسم.
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderFirst);
builder->Writeln(u"First page header.");

builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterFirst);
builder->Writeln(u"First page footer.");

// 2 -  رأس/تذييل "Primary"، الذي يظهر في كل صفحة من القسم.
// يمكننا تجاوز الرأس/التذييل الأساسي برأس/تذييل للصفحة الأولى ورأس/تذييل للصفحة الزوجية.
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
builder->Writeln(u"Primary header.");

builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterPrimary);
builder->Writeln(u"Primary footer.");

builder->MoveToSection(0);
builder->Writeln(u"Page 1.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 2.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 3.");

// كل قسم يحتوي على كائن \"PageSetup\" يحدد خصائص متعلقة بمظهر الصفحة
// مثل الاتجاه، الحجم، والحدود.
// عيّن خاصية "DifferentFirstPageHeaderFooter" إلى "true" لتطبيق الرأس/التذييل الأول على الصفحة الأولى.
// عيّن خاصية "DifferentFirstPageHeaderFooter" إلى "false"
// لجعل الصفحة الأولى تعرض الرأس/التذييل الأساسي.
builder->get_PageSetup()->set_DifferentFirstPageHeaderFooter(differentFirstPageHeaderFooter);

doc->Save(get_ArtifactsDir() + u"PageSetup.DifferentFirstPageHeaderFooter.docx");
```

## انظر أيضًا

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
