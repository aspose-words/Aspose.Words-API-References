---
title: "Aspose::Words::Comment::get_DateTimeUtc طريقة"
linktitle: "get_DateTimeUtc"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Comment::get_DateTimeUtc. يحصل على تاريخ ووقت UTC الذي تم إنشاء التعليق فيه في C++."
type: docs
weight: 7500
url: /ar/cpp/aspose.words/comment/get_datetimeutc/
---
## Comment::get_DateTimeUtc method


يحصل على تاريخ ووقت UTC الذي تم فيه إنشاء التعليق.

```cpp
System::DateTime Aspose::Words::Comment::get_DateTimeUtc()
```


## أمثلة



يعرض كيفية الحصول على تاريخ ووقت UTC.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::DateTime dateTime = System::DateTime::get_Now();
auto comment = System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"J.D.", dateTime);
comment->SetText(u"My comment.");

builder->get_CurrentParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(comment);

doc->Save(get_ArtifactsDir() + u"Comment.UtcDateTime.docx");
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Comment.UtcDateTime.docx");

comment = System::ExplicitCast<Aspose::Words::Comment>(doc->GetChild(Aspose::Words::NodeType::Comment, 0, true));
// تُعيد DateTimeUtc البيانات بدون المللي ثانية.
ASSERT_EQ(dateTime.ToUniversalTime().ToString(u"yyyy-MM-dd hh:mm:ss"), comment->get_DateTimeUtc().ToString(u"yyyy-MM-dd hh:mm:ss"));
```

## انظر أيضًا

* Class [Comment](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
