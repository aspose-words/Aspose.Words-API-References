---
title: "Aspose::Words::Tables::Table::get_DistanceLeft yöntemi"
linktitle: "get_DistanceLeft"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Tables::Table::get_DistanceLeft yöntemi. C++'ta tablo sol kenarı ile çevredeki metin arasındaki mesafeyi puan cinsinden alır veya ayarlar."
type: docs
weight: 20000
url: /tr/cpp/aspose.words.tables/table/get_distanceleft/
---
## Table::get_DistanceLeft method


Tablonun solu ile çevresindeki metin arasındaki mesafeyi, puan cinsinden alır veya ayarlar.

```cpp
double Aspose::Words::Tables::Table::get_DistanceLeft()
```


## Örnekler



Tablo sınırları ile metin arasındaki mesafeyi ayarlamanın nasıl yapılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Table wrapped by text.docx");

System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);
ASPOSE_ASSERT_EQ(25.9, table->get_DistanceTop());
ASPOSE_ASSERT_EQ(25.9, table->get_DistanceBottom());
ASPOSE_ASSERT_EQ(17.3, table->get_DistanceLeft());
ASPOSE_ASSERT_EQ(17.3, table->get_DistanceRight());

// Tablo ile çevredeki metin arasındaki mesafeyi ayarlayın.
table->set_DistanceLeft(24);
table->set_DistanceRight(24);
table->set_DistanceTop(3);
table->set_DistanceBottom(3);

doc->Save(get_ArtifactsDir() + u"Table.DistanceBetweenTableAndText.docx");
```

## Ayrıca Bakınız

* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
