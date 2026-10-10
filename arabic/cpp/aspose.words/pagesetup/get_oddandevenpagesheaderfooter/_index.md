---
title: "Aspose::Words::PageSetup::get_OddAndEvenPagesHeaderFooter طريقة"
linktitle: "get_OddAndEvenPagesHeaderFooter"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::PageSetup::get_OddAndEvenPagesHeaderFooter طريقة. صحيح إذا كان المستند يحتوي على رؤوس وتذييلات مختلفة للصفحات ذات الأرقام الفردية والزوجية في C++."
type: docs
weight: 30000
url: /ar/cpp/aspose.words/pagesetup/get_oddandevenpagesheaderfooter/
---
## PageSetup::get_OddAndEvenPagesHeaderFooter method


صحيح إذا كان المستند يحتوي على رؤوس وتذييلات مختلفة للصفحات ذات الأرقام الفردية والزوجية.

```cpp
bool Aspose::Words::PageSetup::get_OddAndEvenPagesHeaderFooter() const
```


## أمثلة



يظهر كيفية تمكين أو تعطيل رؤوس/تذييلات الصفحات الزوجية.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// فيما يلي نوعان من الرؤوس/التذييلات.
// 1 -  الـ \"Primary\" رأس/تذييل، الذي يظهر في كل صفحة في القسم.
// يمكننا تجاوز الرأس/التذييل الأساسي برأس/تذييل للصفحة الأولى ورأس/تذييل للصفحة الزوجية.
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
builder->Writeln(u"Primary header.");

builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterPrimary);
builder->Writeln(u"Primary footer.");

// 2 -  الـ \"Even\" رأس/تذييل، الذي يظهر في كل صفحة زوجية من هذا القسم.
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderEven);
builder->Writeln(u"Even page header.");

builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterEven);
builder->Writeln(u"Even page footer.");

builder->MoveToSection(0);
builder->Writeln(u"Page 1.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 2.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 3.");

// كل قسم يحتوي على كائن \"PageSetup\" يحدد خصائص متعلقة بمظهر الصفحة
// مثل الاتجاه، الحجم، والحدود.
// عيّن الخاصية \"OddAndEvenPagesHeaderFooter\" إلى \"true\"
// لعرض رأس/تذييل الصفحة الزوجية على الصفحات الزوجية.
// عيّن الخاصية \"OddAndEvenPagesHeaderFooter\" إلى \"false\"
// لعرض الرأس/التذييل الأساسي على الصفحات الزوجية.
builder->get_PageSetup()->set_OddAndEvenPagesHeaderFooter(oddAndEvenPagesHeaderFooter);

doc->Save(get_ArtifactsDir() + u"PageSetup.OddAndEvenPagesHeaderFooter.docx");
```

## انظر أيضًا

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
