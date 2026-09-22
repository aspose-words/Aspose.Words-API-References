---
title: "Aspose::Words::Tables::PreferredWidth::get_Value yöntemi"
linktitle: "get_Value"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Tables::PreferredWidth::get_Value yöntemi. Tercih edilen genişlik değerini alır. Ölçü birimi C++'de Type özelliğinde belirtilir."
type: docs
weight: 7000
url: /tr/cpp/aspose.words.tables/preferredwidth/get_value/
---
## PreferredWidth::get_Value method


Tercih edilen genişlik değerini alır. Ölçü birimi [Type](../get_type/) özelliğinde belirtilir.

```cpp
double Aspose::Words::Tables::PreferredWidth::get_Value() const
```


## Örnekler



Bir tablo hücresinin tercih edilen genişlik türünü ve değerini nasıl doğrulayacağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");

System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);
System::SharedPtr<Aspose::Words::Tables::Cell> firstCell = table->get_FirstRow()->get_FirstCell();

ASSERT_EQ(Aspose::Words::Tables::PreferredWidthType::Percent, firstCell->get_CellFormat()->get_PreferredWidth()->get_Type());
ASPOSE_ASSERT_EQ(11.16, firstCell->get_CellFormat()->get_PreferredWidth()->get_Value());
```

## Ayrıca Bakınız

* Class [PreferredWidth](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
