---
title: "Aspose::Words::Tables::PreferredWidth::get_Type yöntemi"
linktitle: "get_Type"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Tables::PreferredWidth::get_Type yöntemi. C++'de bu tercih edilen genişlik değeri için kullanılan ölçü birimini alır."
type: docs
weight: 6000
url: /tr/cpp/aspose.words.tables/preferredwidth/get_type/
---
## PreferredWidth::get_Type method


Bu tercih edilen genişlik değeri için kullanılan ölçü birimini alır.

```cpp
Aspose::Words::Tables::PreferredWidthType Aspose::Words::Tables::PreferredWidth::get_Type() const
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

* Enum [PreferredWidthType](../../preferredwidthtype/)
* Class [PreferredWidth](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
