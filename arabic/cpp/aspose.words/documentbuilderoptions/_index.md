---
title: "فئة Aspose::Words::DocumentBuilderOptions"
linktitle: "DocumentBuilderOptions"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "فئة Aspose::Words::DocumentBuilderOptions. تسمح بتحديد خيارات إضافية لعملية بناء المستند في C++."
type: docs
weight: 22500
url: /ar/cpp/aspose.words/documentbuilderoptions/
---
## DocumentBuilderOptions class


يسمح بتحديد خيارات إضافية لعملية بناء المستند.

```cpp
class DocumentBuilderOptions : public System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [DocumentBuilderOptions](./documentbuilderoptions/)() |  |
| [get_ContextTableFormatting](./get_contexttableformatting/)() const | صحيح إذا كان التنسيق المطبق على محتوى الجدول لا يؤثر على تنسيق المحتوى الذي يليه. القيمة الافتراضية هي **true**. |
| [get_DesignMode](./get_designmode/)() const | يتطابق مع وضع التصميم في Microsoft Word. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_ContextTableFormatting](./set_contexttableformatting/)(bool) | محدد لـ [Aspose::Words::DocumentBuilderOptions::get_ContextTableFormatting](./get_contexttableformatting/). |
| [set_DesignMode](./set_designmode/)(bool) | يتطابق مع وضع التصميم في Microsoft Word. |
| static [Type](./type/)() |  |

## أمثلة



يعرض كيفية تجاهل تنسيق الجدول للمحتوى التالي.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builderOptions = System::MakeObject<Aspose::Words::DocumentBuilderOptions>();
builderOptions->set_ContextTableFormatting(true);
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc, builderOptions);

// يضيف محتوى قبل الجدول.
// حجم الخط الافتراضي هو 12.
builder->Writeln(u"Font size 12 here.");
builder->StartTable();
builder->InsertCell();
// يغيّر حجم الخط داخل الجدول.
builder->get_Font()->set_Size(5);
builder->Write(u"Font size 5 here");
builder->InsertCell();
builder->Write(u"Font size 5 here");
builder->EndRow();
builder->EndTable();

// إذا كان ContextTableFormatting صحيحًا، فإن تنسيق الجدول لا يُطبق على المحتوى التالي.
// إذا كان ContextTableFormatting خاطئًا، فإن تنسيق الجدول يُطبق على المحتوى التالي.
builder->Writeln(u"Font size 12 here.");

doc->Save(get_ArtifactsDir() + u"Table.ContextTableFormatting.docx");
```

## انظر أيضًا

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
