---
title: "طريقة Aspose::Words::Paragraph::get_BreakIsStyleSeparator"
linktitle: "get_BreakIsStyleSeparator"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Paragraph::get_BreakIsStyleSeparator. True إذا كان فاصل الفقرة هذا هو فاصل نمط. فاصل النمط يسمح لفقرة واحدة أن تتكون من أجزاء لها أنماط فقرة مختلفة في C++."
type: docs
weight: 5000
url: /ar/cpp/aspose.words/paragraph/get_breakisstyleseparator/
---
## Paragraph::get_BreakIsStyleSeparator method


True إذا كان فاصل الفقرة هذا هو [Style](../../style/) Separator. فاصل النمط يسمح لفقرة واحدة أن تتكون من أجزاء لها أنماط فقرة مختلفة.

```cpp
bool Aspose::Words::Paragraph::get_BreakIsStyleSeparator()
```


## أمثلة



يعرض كيفية كتابة النص على نفس سطر عنوان الفهرس (TOC) وجعله لا يظهر في الفهرس.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->InsertTableOfContents(u"\\o \\h \\z \\u");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// أدخل فقرة بنمط سيقوم الفهرس (TOC) بالتقاطه كإدخال.
builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading1);

// كلا السلسلتين في نفس الفقرة وبالتالي سيظهران في نفس إدخال الفهرس (TOC).
builder->Write(u"Heading 1. ");
builder->Write(u"Will appear in the TOC. ");

// إذا أدخلنا فاصل نمط، يمكننا كتابة المزيد من النص في نفس الفقرة
// واستخدام نمط مختلف دون أن يظهر في الفهرس.
// إذا استخدمنا نمط عنوان بعد الفاصل، يمكننا إنشاء إدخالات فهرس متعددة من سطر نص واحد في المستند.
builder->InsertStyleSeparator();
builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Quote);
builder->Write(u"Won't appear in the TOC. ");

ASSERT_TRUE(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_BreakIsStyleSeparator());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Paragraph.BreakIsStyleSeparator.docx");
```

## انظر أيضًا

* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
