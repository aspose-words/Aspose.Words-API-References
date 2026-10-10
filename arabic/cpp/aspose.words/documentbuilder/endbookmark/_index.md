---
title: "Aspose::Words::DocumentBuilder::EndBookmark method"
linktitle: "EndBookmark"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::DocumentBuilder::EndBookmark method. يحدد الموضع الحالي في المستند كنهاية إشارة مرجعية في C++."
type: docs
weight: 4000
url: /ar/cpp/aspose.words/documentbuilder/endbookmark/
---
## DocumentBuilder::EndBookmark method


يُعلِّم الموضع الحالي في المستند كنهاية إشارة مرجعية.

```cpp
System::SharedPtr<Aspose::Words::BookmarkEnd> Aspose::Words::DocumentBuilder::EndBookmark(const System::String &bookmarkName)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| bookmarkName | const System::String\& | اسم الإشارة المرجعية. |

### ReturnValue

عقدة نهاية الإشارة المرجعية التي تم إنشاؤها للتو.
## ملاحظات


يمكن أن تتداخل العلامات المرجعية في المستند وتغطي أي نطاق. لإنشاء علامة مرجعية صالحة تحتاج إلى استدعاء كل من [StartBookmark()](../) و [EndBookmark()](../) مع نفس المعامل *bookmarkName*.

سيتم تجاهل العلامات المرجعية المشكّلة بشكل سيء أو التي لها أسماء مكررة عند حفظ المستند.

## أمثلة



يوضح كيفية إنشاء علامة مرجعية.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// تحتاج العلامة المرجعية الصالحة إلى أن يحتوي نص جسم المستند على
// عقد BookmarkStart و BookmarkEnd التي تم إنشاؤها باسم علامة مرجعية متطابق.
builder->StartBookmark(u"MyBookmark");
builder->Writeln(u"Hello world!");
builder->EndBookmark(u"MyBookmark");

ASSERT_EQ(1, doc->get_Range()->get_Bookmarks()->get_Count());
ASSERT_EQ(u"MyBookmark", doc->get_Range()->get_Bookmarks()->idx_get(0)->get_Name());
ASSERT_EQ(u"Hello world!", doc->get_Range()->get_Bookmarks()->idx_get(0)->get_Text().Trim());
```


يوضح كيفية إدراج ارتباط تشعبي يشير إلى علامة مرجعية محلية.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->StartBookmark(u"Bookmark1");
builder->Write(u"Bookmarked text. ");
builder->EndBookmark(u"Bookmark1");
builder->Writeln(u"Text outside of the bookmark.");

// أدرج حقل HYPERLINK يربط بالعلامة المرجعية. يمكننا تمرير مفاتيح الحقل
// إلى طريقة "InsertHyperlink" كجزء من الوسيط الذي يحتوي على اسم العلامة المرجعية المشار إليها.
builder->get_Font()->set_Color(System::Drawing::Color::get_Blue());
builder->get_Font()->set_Underline(Aspose::Words::Underline::Single);
auto hyperlink = System::ExplicitCast<Aspose::Words::Fields::FieldHyperlink>(builder->InsertHyperlink(u"Link to Bookmark1", u"Bookmark1", true));
hyperlink->set_ScreenTip(u"Hyperlink Tip");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertHyperlinkToLocalBookmark.docx");
```

## انظر أيضًا

* Class [BookmarkEnd](../../bookmarkend/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
