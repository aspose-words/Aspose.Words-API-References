---
title: "طريقة Aspose::Words::DocumentBuilder::EndColumnBookmark"
linktitle: "EndColumnBookmark"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::DocumentBuilder::EndColumnBookmark طريقة. يحدد الموضع الحالي في المستند كنهاية إشارة مرجعية للعمود. يجب أن يكون الموضع داخل خلية جدول في C++."
type: docs
weight: 5000
url: /ar/cpp/aspose.words/documentbuilder/endcolumnbookmark/
---
## DocumentBuilder::EndColumnBookmark method


يُعلِّم الموضع الحالي في المستند كنهاية إشارة مرجعية للعمود. يجب أن يكون الموضع داخل خلية جدول.

```cpp
System::SharedPtr<Aspose::Words::BookmarkEnd> Aspose::Words::DocumentBuilder::EndColumnBookmark(const System::String &bookmarkName)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| bookmarkName | const System::String\& | اسم الإشارة المرجعية. |

### ReturnValue

عقدة نهاية الإشارة المرجعية التي تم إنشاؤها للتو.
## ملاحظات


تغطي إشارة مرجعية للعمود عمودًا واحدًا أو أكثر في نطاق من الصفوف. لإنشاء إشارة مرجعية صالحة تحتاج إلى استدعاء كل من [StartColumnBookmark()](../) و[EndColumnBookmark()](../) بنفس معامل *bookmarkName*.

سيتم تجاهل العلامات المرجعية المشكّلة بشكل سيء أو التي لها أسماء مكررة عند حفظ المستند.

قد يختلف الموضع الفعلي للعقدة [BookmarkEnd](../../bookmarkend/) التي تم إدراجها عن موضع مُنشئ المستند الحالي.

## أمثلة



يوضح كيفية إنشاء إشارة مرجعية للعمود.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->StartTable();

builder->InsertCell();
// سيتم وضع إشارة مرجعية على الخلايا 1,2,4,5.
builder->StartColumnBookmark(u"MyBookmark_1");
// سيتم تجاهل العلامات المرجعية المشكّلة بشكل سيء أو التي لها أسماء مكررة عند حفظ المستند.
builder->StartColumnBookmark(u"MyBookmark_1");
builder->StartColumnBookmark(u"BadStartBookmark");
builder->Write(u"Cell 1");

builder->InsertCell();
builder->Write(u"Cell 2");

builder->InsertCell();
builder->Write(u"Cell 3");

builder->EndRow();

builder->InsertCell();
builder->Write(u"Cell 4");

builder->InsertCell();
builder->Write(u"Cell 5");
builder->EndColumnBookmark(u"MyBookmark_1");
builder->EndColumnBookmark(u"MyBookmark_1");

ASSERT_THROW(static_cast<std::function<void()>>([&builder]() -> void
{
    builder->EndColumnBookmark(u"BadEndBookmark");

builder->InsertCell();
builder->Write(u"Cell 6");

builder->EndRow();
builder->EndTable();

doc->Save(get_ArtifactsDir() + u"Bookmarks.CreateColumnBookmark.docx");
```

## انظر أيضًا

* Class [BookmarkEnd](../../bookmarkend/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
