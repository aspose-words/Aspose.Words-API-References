---
title: "طريقة Aspose::Words::DocumentBuilder::InsertHyperlink"
linktitle: "InsertHyperlink"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::DocumentBuilder::InsertHyperlink. تُدرج ارتباطًا تشعبيًا في المستند بلغة C++."
type: docs
weight: 38000
url: /ar/cpp/aspose.words/documentbuilder/inserthyperlink/
---
## DocumentBuilder::InsertHyperlink method


يقوم بإدراج ارتباط تشعبي في المستند.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::DocumentBuilder::InsertHyperlink(const System::String &displayText, const System::String &urlOrBookmark, bool isBookmark)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| displayText | const System::String\& | نص الرابط الذي سيُعرض في المستند. |
| urlOrBookmark | const System::String\& | وجهة الارتباط. يمكن أن تكون عنوان URL أو اسم إشارة مرجعية داخل المستند. هذه الطريقة دائمًا تضيف علامات اقتباس في بداية ونهاية عنوان URL. |
| isBookmark | bool | **true** إذا كان المعامل السابق اسم إشارة مرجعية داخل المستند؛ **false** إذا كان المعامل السابق عنوان URL. |

### ReturnValue

كائن [Field](../../../aspose.words.fields/field/) الذي يمثل الحقل المُدرج.
## ملاحظات


لاحظ أنه يجب عليك تحديد تنسيق الخط لنص الارتباط التشعبي صراحةً باستخدام خاصية [Font](../get_font/).

هذه الطريقة تستدعي داخليًا الدالة [InsertField()](../) لإدراج حقل HYPERLINK في مستند MS Word.

## أمثلة



يظهر كيفية إدراج حقل ارتباط تشعبي.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"For more information, please visit the ");

// أدرج ارتباطًا تشعبيًا وأبرزه بتنسيق مخصص.
// سيكون الارتباط التشعبي قطعة نصية قابلة للنقر ستنقلنا إلى الموقع المحدد في عنوان URL.
builder->get_Font()->set_Color(System::Drawing::Color::get_Blue());
builder->get_Font()->set_Underline(Aspose::Words::Underline::Single);
builder->InsertHyperlink(u"Google website", u"https://www.google.com", false);
builder->get_Font()->ClearFormatting();
builder->Writeln(u".");

// ستؤدي عملية الضغط على Ctrl + النقر الأيسر على الرابط في النص داخل Microsoft Word إلى الانتقال إلى عنوان URL عبر نافذة متصفح ويب جديدة.
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertHyperlink.docx");
```


يوضح كيفية استخدام مكدس تنسيق منشئ المستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// قم بإعداد تنسيق الخط، ثم اكتب النص الذي يسبق الارتباط.
builder->get_Font()->set_Name(u"Arial");
builder->get_Font()->set_Size(24);
builder->Write(u"To visit Google, hold Ctrl and click ");

// احفظ تكوين التنسيق الحالي على المكدس.
builder->PushFont();

// غيّر تنسيق المنشئ الحالي بتطبيق نمط جديد.
builder->get_Font()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Hyperlink);
builder->InsertHyperlink(u"here", u"http://www.google.com", false);

ASSERT_EQ(System::Drawing::Color::get_Blue().ToArgb(), builder->get_Font()->get_Color().ToArgb());
ASSERT_EQ(Aspose::Words::Underline::Single, builder->get_Font()->get_Underline());

// استعد تنسيق الخط الذي حفظناه مسبقًا وأزل العنصر من المكدس.
builder->PopFont();

ASSERT_EQ(System::Drawing::Color::Empty.ToArgb(), builder->get_Font()->get_Color().ToArgb());
ASSERT_EQ(Aspose::Words::Underline::None, builder->get_Font()->get_Underline());

builder->Write(u". We hope you enjoyed the example.");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.PushPopFont.docx");
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

* Class [Field](../../../aspose.words.fields/field/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
