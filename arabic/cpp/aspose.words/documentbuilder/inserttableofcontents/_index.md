---
title: "Aspose::Words::DocumentBuilder::InsertTableOfContents method"
linktitle: "InsertTableOfContents"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::DocumentBuilder::InsertTableOfContents method. يدرج حقل فهرس (table of contents) في المستند بلغة C++."
type: docs
weight: 48000
url: /ar/cpp/aspose.words/documentbuilder/inserttableofcontents/
---
## DocumentBuilder::InsertTableOfContents method


يدرج حقل فهرس (table of contents) في المستند.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::DocumentBuilder::InsertTableOfContents(const System::String &switches)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| المفاتيح | const System::String\& | مفاتيح حقل الفهرس. |
## ملاحظات


تقوم هذه الطريقة بإدراج حقل فهرس (table of contents) في المستند في الموضع الحالي.

يمكن إنشاء فهرس في مستند Word بعدة طرق وتنسيقه باستخدام مجموعة متنوعة من الخيارات. طريقة إنشاء الفهرس وعرضه بواسطة Microsoft Word يتم التحكم فيها بواسطة مفاتيح الحقل.

أسهل طريقة لتحديد المفاتيح هي إدراج وتكوين فهرس في مستند Word باستخدام قائمة Insert->Reference->Index و[Tables](../../../aspose.words.tables/)، ثم تشغيل عرض رموز الحقل لرؤية المفاتيح. يمكنك الضغط على Alt+F9 في Microsoft Word لتبديل عرض رموز الحقل تشغيلًا أو إيقافًا.

على سبيل المثال، بعد إنشاء فهرس، يتم إدراج الحقل التالي في المستند: **%{ TOC \o "1-3" \h \z }**. يمكنك نسخ **%\o "1-3" \h \z** واستخدامه كمعامل للمفاتيح.

لاحظ أن [InsertTableOfContents()](../) سيقوم فقط بإدراج حقل فهرس، لكنه لن يبني الفهرس فعليًا. يتم بناء الفهرس بواسطة Microsoft Word عند تحديث الحقل.

إذا قمت بإدراج فهرس باستخدام هذه الطريقة ثم فتحت الملف في Microsoft Word، لن ترى الفهرس لأن حقل TOC لم يتم تحديثه بعد.

في Microsoft Word، لا يتم تحديث الحقول تلقائيًا عند فتح المستند، ولكن يمكنك تحديث الحقول في أي وقت بالضغط على F9.

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

* Class [Field](../../../aspose.words.fields/field/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
