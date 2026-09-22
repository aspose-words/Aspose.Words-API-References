---
title: "Aspose::Words::Tables::PreferredWidth class"
linktitle: "PreferredWidth"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Tables::PreferredWidth class. يمثل قيمة ووحدة قياسها المستخدمة لتحديد العرض المفضل لجدول أو خلية. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 4000
url: /ar/cpp/aspose.words.tables/preferredwidth/
---
## PreferredWidth class


يمثل قيمة ووحدة قياسها المستخدمة لتحديد العرض المفضل لجدول أو خلية. لمعرفة المزيد، زر مقالة الوثائق [Working with Tables](https://docs.aspose.com/words/cpp/working-with-tables/).

```cpp
class PreferredWidth : public System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| static [Auto](./auto/)() | يرجع كائنًا يمثل القيمة \"العرض المفضل غير محدد\". |
| [Equals](./equals/)(const System::SharedPtr\<Aspose::Words::Tables::PreferredWidth\>\&) | يحدد ما إذا كان [PreferredWidth](./) المحدد يساوي في القيمة [PreferredWidth](./) الحالي. |
| [Equals](./equals/)(System::SharedPtr\<System::Object\>) override | يحدد ما إذا كان الكائن المحدد مساوٍ في القيمة للكائن الحالي. |
| static [FromPercent](./frompercent/)(double) | طريقة إنشاء تُرجع كائنًا جديدًا يمثل عرضًا مفضلاً محددًا كنسبة مئوية. |
| static [FromPoints](./frompoints/)(double) | طريقة إنشاء تُرجع كائنًا جديدًا يمثل عرضًا مفضلاً محددًا باستخدام عدد من النقاط. |
| [get_Type](./get_type/)() const | يحصل على وحدة القياس المستخدمة لهذه القيمة من العرض المفضل. |
| [get_Value](./get_value/)() const | يحصل على قيمة العرض المفضل. وحدة القياس محددة في الخاصية [Type](./get_type/). |
| [GetHashCode](./gethashcode/)() const override | يعمل كدالة تجزئة لهذا النوع. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [ToString](./tostring/)() const override | يعيد سلسلة سهلة القراءة تعرض قيمة هذا الكائن. |
| static [Type](./type/)() |  |
## ملاحظات


يمكن تحديد العرض المفضل كنسبة مئوية أو عدد نقاط أو قيمة خاصة \"none/auto\".

كائنات هذه الفئة غير قابلة للتغيير.

## أمثلة



يوضح كيفية ضبط جدول ليتناسب تلقائيًا مع 50٪ من عرض الصفحة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Cell #1");
builder->InsertCell();
builder->Write(u"Cell #2");
builder->InsertCell();
builder->Write(u"Cell #3");

table->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPercent(50));

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertTableWithPreferredWidth.docx");
```


يوضح كيفية تعيين عرض مفضل لخلايا الجدول.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();

// هناك طريقتان لتطبيق الفئة \"PreferredWidth\" على خلايا الجدول.
// 1 -  تعيين عرض مفضل ثابت بناءً على النقاط:
builder->InsertCell();
builder->get_CellFormat()->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPoints(40));
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightYellow());
builder->Writeln(System::String::Format(u"Cell with a width of {0}.", builder->get_CellFormat()->get_PreferredWidth()));

// 2 -  تعيين عرض مفضل نسبي بناءً على نسبة من عرض الجدول:
builder->InsertCell();
builder->get_CellFormat()->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPercent(20));
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightBlue());
builder->Writeln(System::String::Format(u"Cell with a width of {0}.", builder->get_CellFormat()->get_PreferredWidth()));

builder->InsertCell();

// الخلية التي لا يُحدد لها عرض مفضل ستشغل باقي المساحة المتاحة.
builder->get_CellFormat()->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::Auto());

// كل تكوين لخاصية \"PreferredWidth\" ينشئ كائنًا جديدًا.
ASSERT_NE(System::ObjectExt::GetHashCode(table->get_FirstRow()->get_Cells()->idx_get(1)->get_CellFormat()->get_PreferredWidth()), System::ObjectExt::GetHashCode(builder->get_CellFormat()->get_PreferredWidth()));

builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightGreen());
builder->Writeln(u"Automatically sized cell.");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertCellsWithPreferredWidths.docx");
```

## انظر أيضًا

* Namespace [Aspose::Words::Tables](../)
* Library [Aspose.Words for C++](../../)
