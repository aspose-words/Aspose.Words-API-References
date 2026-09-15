---
title: "طريقة Aspose::Words::PageSetup::get_Bidi"
linktitle: "get_Bidi"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::PageSetup::get_Bidi. يحدد أن هذا القسم يحتوي على نص ثنائي الاتجاه (نصوص معقدة) في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words/pagesetup/get_bidi/
---
## PageSetup::get_Bidi method


يحدد أن هذا القسم يحتوي على نص ثنائي الاتجاه (نصوص معقدة).

```cpp
bool Aspose::Words::PageSetup::get_Bidi()
```

## ملاحظات


عند **true**، تُرتّب الأعمدة في هذا القسم من اليمين إلى اليسار.

## أمثلة



يظهر كيفية ضبط ترتيب أعمدة النص في قسم.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();
pageSetup->get_TextColumns()->SetCount(3);

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Write(u"Column 1.");
builder->InsertBreak(Aspose::Words::BreakType::ColumnBreak);
builder->Write(u"Column 2.");
builder->InsertBreak(Aspose::Words::BreakType::ColumnBreak);
builder->Write(u"Column 3.");

// قم بتعيين خاصية "Bidi" إلى "true" لترتيب الأعمدة بدءًا من الجانب الأيمن للصفحة.
// سيتطابق ترتيب الأعمدة مع اتجاه النص من اليمين إلى اليسار.
// قم بتعيين خاصية "Bidi" إلى "false" لترتيب الأعمدة بدءًا من الجانب الأيسر للصفحة.
// سيتطابق ترتيب الأعمدة مع اتجاه النص من اليسار إلى اليمين.
pageSetup->set_Bidi(reverseColumns);

doc->Save(get_ArtifactsDir() + u"PageSetup.Bidi.docx");
```

## انظر أيضًا

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
