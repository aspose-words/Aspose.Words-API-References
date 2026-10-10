---
title: "طريقة Aspose::Words::PageSetup::get_RestartPageNumbering"
linktitle: "get_RestartPageNumbering"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::PageSetup::get_RestartPageNumbering. صحيحة إذا كان ترقيم الصفحات يعيد البدء في بداية القسم في C++."
type: docs
weight: 38000
url: /ar/cpp/aspose.words/pagesetup/get_restartpagenumbering/
---
## PageSetup::get_RestartPageNumbering method


صحيح إذا كان ترقيم الصفحات يعيد البدء في بداية القسم.

```cpp
bool Aspose::Words::PageSetup::get_RestartPageNumbering()
```


## أمثلة



يظهر كيفية إعداد ترقيم الصفحات في قسم.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Section 1, page 1.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Section 1, page 2.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Section 1, page 3.");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Writeln(u"Section 2, page 1.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Section 2, page 2.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Section 2, page 3.");

// انقل مُنشئ المستند إلى الرأس الأساسي للقسم الأول،
// الذي سيُظهره كل صفحة في ذلك القسم.
builder->MoveToSection(0);
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);

// أدرج حقل PAGE، الذي سيعرض رقم الصفحة الحالية.
builder->Write(u"Page ");
builder->InsertField(u"PAGE", u"");

// قم بتكوين القسم بحيث يبدأ عدد الصفحات الذي تعرضه حقول PAGE من 5.
// أيضًا، قم بتكوين جميع حقول PAGE لعرض أرقام صفحاتها باستخدام الأرقام الرومانية الكبيرة.
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();
pageSetup->set_RestartPageNumbering(true);
pageSetup->set_PageStartingNumber(5);
pageSetup->set_PageNumberStyle(Aspose::Words::NumberStyle::UppercaseRoman);

// أنشئ رأسًا أساسيًا آخر للقسم الثاني، مع حقل PAGE آخر.
builder->MoveToSection(1);
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
builder->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);
builder->Write(u" - ");
builder->InsertField(u"PAGE", u"");
builder->Write(u" - ");

// قم بتكوين القسم بحيث يبدأ عدد الصفحات الذي تعرضه حقول PAGE من 10.
// أيضًا، قم بتكوين جميع حقول PAGE لعرض أرقام صفحاتها باستخدام الأرقام العربية.
pageSetup = doc->get_Sections()->idx_get(1)->get_PageSetup();
pageSetup->set_PageStartingNumber(10);
pageSetup->set_RestartPageNumbering(true);
pageSetup->set_PageNumberStyle(Aspose::Words::NumberStyle::Arabic);

doc->Save(get_ArtifactsDir() + u"PageSetup.PageNumbering.docx");
```

## انظر أيضًا

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
