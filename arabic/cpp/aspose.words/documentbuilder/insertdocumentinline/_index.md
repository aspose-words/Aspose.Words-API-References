---
title: "طريقة Aspose::Words::DocumentBuilder::InsertDocumentInline"
linktitle: "InsertDocumentInline"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::DocumentBuilder::InsertDocumentInline. تُدرج مستندًا داخل السطر في موضع المؤشر في C++."
type: docs
weight: 33500
url: /ar/cpp/aspose.words/documentbuilder/insertdocumentinline/
---
## DocumentBuilder::InsertDocumentInline method


يدرج مستندًا مضمنًا في موضع المؤشر.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::DocumentBuilder::InsertDocumentInline(const System::SharedPtr<Aspose::Words::Document> &srcDoc, Aspose::Words::ImportFormatMode importFormatMode, const System::SharedPtr<Aspose::Words::ImportFormatOptions> &importFormatOptions)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| srcDoc | const System::SharedPtr\<Aspose::Words::Document\>\& | المستند المصدر للإدراج. |
| importFormatMode | Aspose::Words::ImportFormatMode | يحدد كيفية دمج تنسيق الأنماط المتصادمة. |
| importFormatOptions | const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\& | يسمح بتحديد الخيارات التي تؤثر على تنسيق المستند الناتج. |

### ReturnValue

العقدة الأولى للمحتوى المُدرج.
## ملاحظات


تحاكي هذه الطريقة سلوك MS Word، كما لو تم الضغط على CTRL+'A' (تحديد كل المحتوى)، ثم CTRL+'C' (نسخ المحدد إلى الذاكرة المؤقتة) داخل مستند واحد، ثم CTRL+'V' (إدراج المحتوى من الذاكرة المؤقتة) داخل مستند آخر.

على عكس [InsertDocument()](../) تقوم هذه الطريقة بنقل محتوى الفقرة في المستند الوجهة، التي يُدرج قبلها المستند المصدر، إلى الفقرة الأخيرة في المستند المصدر المُدرج. في الواقع، يعني ذلك إزالة فاصل الفقرة للفقرة الأخيرة المُدرجة.

ملاحظة، إذا لم يكن العقدة الأخيرة في المستند المصدر فقرة، فلن يتم تنفيذ أي شيء.

## أمثلة



يوضح كيفية إدراج مستند داخل السطر في موضع المؤشر.
```cpp
auto srcDoc = System::MakeObject<Aspose::Words::DocumentBuilder>();
srcDoc->Write(u"[src content]");

// إنشاء مستند الوجهة.
auto dstDoc = System::MakeObject<Aspose::Words::DocumentBuilder>();
dstDoc->Write(u"Before ");
dstDoc->InsertNode(System::MakeObject<Aspose::Words::BookmarkStart>(dstDoc->get_Document(), u"src_place"));
dstDoc->InsertNode(System::MakeObject<Aspose::Words::BookmarkEnd>(dstDoc->get_Document(), u"src_place"));
dstDoc->Write(u" after");

ASSERT_EQ(u"Before  after", dstDoc->get_Document()->GetText().TrimEnd(System::MakeObject<System::Array<char16_t>>(0)));

// إدراج المستند المصدر داخل المستند الوجهة داخل السطر.
dstDoc->MoveToBookmark(u"src_place");
dstDoc->InsertDocumentInline(srcDoc->get_Document(), Aspose::Words::ImportFormatMode::UseDestinationStyles, System::MakeObject<Aspose::Words::ImportFormatOptions>());

ASSERT_EQ(u"Before [src content] after", dstDoc->get_Document()->GetText().TrimEnd(System::MakeObject<System::Array<char16_t>>(0)));
```

## انظر أيضًا

* Class [Node](../../node/)
* Class [Document](../../document/)
* Enum [ImportFormatMode](../../importformatmode/)
* Class [ImportFormatOptions](../../importformatoptions/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
