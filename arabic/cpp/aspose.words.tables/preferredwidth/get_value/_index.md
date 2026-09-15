---
title: "Aspose::Words::Tables::PreferredWidth::get_Value طريقة"
linktitle: "get_Value"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Tables::PreferredWidth::get_Value طريقة. يحصل على قيمة العرض المفضل. وحدة القياس محددة في الخاصية Type في C++."
type: docs
weight: 7000
url: /ar/cpp/aspose.words.tables/preferredwidth/get_value/
---
## PreferredWidth::get_Value method


يحصل على قيمة العرض المفضل. وحدة القياس محددة في الخاصية [Type](../get_type/).

```cpp
double Aspose::Words::Tables::PreferredWidth::get_Value() const
```


## أمثلة



يظهر كيفية التحقق من نوع العرض المفضل وقيمته لخلية جدول.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");

System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);
System::SharedPtr<Aspose::Words::Tables::Cell> firstCell = table->get_FirstRow()->get_FirstCell();

ASSERT_EQ(Aspose::Words::Tables::PreferredWidthType::Percent, firstCell->get_CellFormat()->get_PreferredWidth()->get_Type());
ASPOSE_ASSERT_EQ(11.16, firstCell->get_CellFormat()->get_PreferredWidth()->get_Value());
```

## انظر أيضًا

* Class [PreferredWidth](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
