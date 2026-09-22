---
title: "Aspose::Words::Tables::Table::get_AllowCellSpacing طريقة"
linktitle: "get_AllowCellSpacing"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Tables::Table::get_AllowCellSpacing طريقة. يحصل على أو يضبط خيار \"السماح بالتباعد بين الخلايا\" في C++."
type: docs
weight: 13000
url: /ar/cpp/aspose.words.tables/table/get_allowcellspacing/
---
## Table::get_AllowCellSpacing method


يحصل أو يضبط خيار \"Allow spacing between cells\".

```cpp
bool Aspose::Words::Tables::Table::get_AllowCellSpacing()
```


## أمثلة



يظهر كيفية تمكين التباعد بين الخلايا الفردية في جدول.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Animal");
builder->InsertCell();
builder->Write(u"Class");
builder->EndRow();
builder->InsertCell();
builder->Write(u"Dog");
builder->InsertCell();
builder->Write(u"Mammal");
builder->EndTable();

table->set_CellSpacing(3);

// عيّن الخاصية "AllowCellSpacing" إلى "true" لتمكين التباعد بين الخلايا
// بقيمة مساوية لقيمة الخاصية "CellSpacing"، بالنقاط.
// عيّن الخاصية "AllowCellSpacing" إلى "false" لتعطيل التباعد بين الخلايا
// وتجاهل قيمة الخاصية "CellSpacing".
table->set_AllowCellSpacing(allowCellSpacing);

doc->Save(get_ArtifactsDir() + u"Table.AllowCellSpacing.html");

// تعديل الخاصية "CellSpacing" سيفعل تلقائيًا التباعد بين الخلايا.
table->set_CellSpacing(5);

ASSERT_TRUE(table->get_AllowCellSpacing());
```

## انظر أيضًا

* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
