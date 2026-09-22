---
title: "طريقة Aspose::Words::ParagraphFormat::get_StyleIdentifier"
linktitle: "get_StyleIdentifier"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::ParagraphFormat::get_StyleIdentifier. يحصل على أو يضبط معرف النمط المستقل عن اللغة للفقرة المطبقة على هذا التنسيق في C++."
type: docs
weight: 36000
url: /ar/cpp/aspose.words/paragraphformat/get_styleidentifier/
---
## ParagraphFormat::get_StyleIdentifier method


يحصل أو يعيّن معرف النمط المستقل عن اللغة لنمط الفقرة المطبق على هذا التنسيق.

```cpp
Aspose::Words::StyleIdentifier Aspose::Words::ParagraphFormat::get_StyleIdentifier()
```


## أمثلة



يوضح كيفية إدراج جدول محتويات (TOC) في مستند باستخدام أنماط العناوين كمدخلات.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// إدراج جدول محتويات للصفحة الأولى من المستند.
// تكوين الجدول لالتقاط الفقرات التي تحتوي على عناوين من المستوى 1 إلى 3.
// أيضًا، اضبط مدخلاته لتكون روابط تشعبية ستأخذنا
// إلى موقع العنوان عند النقر بزر الفأرة الأيسر في Microsoft Word.
builder->InsertTableOfContents(u"\\o \"1-3\" \\h \\z \\u");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// قم بملء جدول المحتويات بإضافة فقرات باستخدام أنماط العناوين.
// كل عنوان من هذا النوع بمستوى بين 1 و 3 سيُنشئ مدخلاً في الجدول.
builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading1);
builder->Writeln(u"Heading 1");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading2);
builder->Writeln(u"Heading 1.1");
builder->Writeln(u"Heading 1.2");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading1);
builder->Writeln(u"Heading 2");
builder->Writeln(u"Heading 3");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading2);
builder->Writeln(u"Heading 3.1");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading3);
builder->Writeln(u"Heading 3.1.1");
builder->Writeln(u"Heading 3.1.2");
builder->Writeln(u"Heading 3.1.3");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading4);
builder->Writeln(u"Heading 3.1.3.1");
builder->Writeln(u"Heading 3.1.3.2");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading2);
builder->Writeln(u"Heading 3.2");
builder->Writeln(u"Heading 3.3");

// جدول المحتويات هو حقل من نوع يحتاج إلى تحديث لإظهار نتيجة محدثة.
doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertToc.docx");
```

## انظر أيضًا

* Enum [StyleIdentifier](../../styleidentifier/)
* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
