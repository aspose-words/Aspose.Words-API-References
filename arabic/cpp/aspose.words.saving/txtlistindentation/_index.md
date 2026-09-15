---
title: "فئة Aspose::Words::Saving::TxtListIndentation"
linktitle: "TxtListIndentation"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "فئة Aspose::Words::Saving::TxtListIndentation. تحدد كيفية إزاحة مستويات القوائم عند تصدير المستند إلى تنسيق النص. لمعرفة المزيد، قم بزيارة مقالة الوثائق في C++."
type: docs
weight: 32000
url: /ar/cpp/aspose.words.saving/txtlistindentation/
---
## TxtListIndentation class


تحدد كيفية إزاحة مستويات القوائم عند تصدير المستند إلى تنسيق [نص](../../aspose.words/saveformat/). لمعرفة المزيد، قم بزيارة مقالة الوثائق [حفظ المستند](https://docs.aspose.com/words/cpp/save-a-document/).

```cpp
class TxtListIndentation : public System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [get_Character](./get_character/)() const | يحصل أو يعيّن أي حرف يُستخدم لإزاحة مستويات القوائم. القيمة الافتراضية هي '\0'، وهذا يعني عدم وجود إزاحة. |
| [get_Count](./get_count/)() const | يحصل أو يعيّن عدد [حرف](./get_character/) المستخدم كإزاحة لكل مستوى قائمة. القيمة الافتراضية هي 0، وهذا يعني عدم وجود إزاحة. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Character](./set_character/)(char16_t) | مُعيّن لـ [Aspose::Words::Saving::TxtListIndentation::get_Character](./get_character/). |
| [set_Count](./set_count/)(int32_t) | مُعيّن لـ [Aspose::Words::Saving::TxtListIndentation::get_Count](./get_count/). |
| [TxtListIndentation](./txtlistindentation/)() |  |
| static [Type](./type/)() |  |

## أمثلة



يعرض كيفية تكوين إزاحة القوائم عند حفظ المستند كنص عادي.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// إنشاء قائمة بثلاث مستويات من الإزاحة.
builder->get_ListFormat()->ApplyNumberDefault();
builder->Writeln(u"Item 1");
builder->get_ListFormat()->ListIndent();
builder->Writeln(u"Item 2");
builder->get_ListFormat()->ListIndent();
builder->Write(u"Item 3");

// إنشاء كائن "TxtSaveOptions"، والذي يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
// لتعديل طريقة حفظ المستند كنص عادي.
auto txtSaveOptions = System::MakeObject<Aspose::Words::Saving::TxtSaveOptions>();

// قم بتعيين خاصية \"Character\" لتحديد حرف لاستخدامه
// للتعبئة التي تحاكي إزاحة القوائم في النص العادي.
txtSaveOptions->get_ListIndentation()->set_Character(u' ');

// قم بتعيين خاصية \"Count\" لتحديد عدد المرات
// لوضع حرف التعبئة لكل مستوى إزاحة قائمة.
txtSaveOptions->get_ListIndentation()->set_Count(3);

doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.TxtListIndentation.txt", txtSaveOptions);

System::String docText = System::IO::File::ReadAllText(get_ArtifactsDir() + u"TxtSaveOptions.TxtListIndentation.txt");
System::String newLine = System::Environment::get_NewLine();

ASSERT_EQ(System::String::Format(u"1. Item 1{0}", newLine) + System::String::Format(u"   a. Item 2{0}", newLine) + System::String::Format(u"      i. Item 3{0}", newLine), docText);
```

## انظر أيضًا

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
