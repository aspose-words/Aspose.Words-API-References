---
title: "Aspose::Words::Tables::PreferredWidth::get_Type طريقة"
linktitle: "get_Type"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Tables::PreferredWidth::get_Type طريقة. يحصل على وحدة القياس المستخدمة لهذه القيمة من العرض المفضل في C++."
type: docs
weight: 6000
url: /ar/cpp/aspose.words.tables/preferredwidth/get_type/
---
## PreferredWidth::get_Type method


يحصل على وحدة القياس المستخدمة لهذه القيمة من العرض المفضل.

```cpp
Aspose::Words::Tables::PreferredWidthType Aspose::Words::Tables::PreferredWidth::get_Type() const
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

* Enum [PreferredWidthType](../../preferredwidthtype/)
* Class [PreferredWidth](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
