---
title: "طريقة Aspose::Words::Tables::Table::get_AbsoluteHorizontalDistance"
linktitle: "get_AbsoluteHorizontalDistance"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Tables::Table::get_AbsoluteHorizontalDistance. تحصل أو تعيين موضع الجدول العائم الأفقي المطلق المحدد بخصائص الجدول، بالنقاط. القيمة الافتراضية هي 0 في C++."
type: docs
weight: 9000
url: /ar/cpp/aspose.words.tables/table/get_absolutehorizontaldistance/
---
## Table::get_AbsoluteHorizontalDistance method


يحصل أو يضبط موضع الجدول العائم الأفقي المطلق المحدد بخصائص الجدول، بالنقاط. القيمة الافتراضية هي 0.

```cpp
double Aspose::Words::Tables::Table::get_AbsoluteHorizontalDistance()
```


## أمثلة



يظهر كيفية تعيين موقع الجداول العائمة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Table 1, cell 1");
builder->EndTable();
table->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPoints(300));

// عيّن موقع الجدول إلى مكان على الصفحة، مثل، في هذه الحالة، الزاوية السفلية اليمنى.
table->set_RelativeVerticalAlignment(Aspose::Words::Drawing::VerticalAlignment::Bottom);
table->set_RelativeHorizontalAlignment(Aspose::Words::Drawing::HorizontalAlignment::Right);

table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Table 2, cell 1");
builder->EndTable();
table->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPoints(300));

// يمكننا أيضًا تعيين إزاحة أفقية ورأسية بالنقاط من موقع الفقرة حيث أدخلنا الجدول.
table->set_AbsoluteVerticalDistance(50);
table->set_AbsoluteHorizontalDistance(100);

doc->Save(get_ArtifactsDir() + u"Table.ChangeFloatingTableProperties.docx");
```

## انظر أيضًا

* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
