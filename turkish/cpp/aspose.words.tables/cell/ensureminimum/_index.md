---
title: "Aspose::Words::Tables::Cell::EnsureMinimum yöntemi"
linktitle: "EnsureMinimum"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Tables::Cell::EnsureMinimum yöntemi. Son alt öğe bir paragraf değilse, C++'ta bir boş paragraf oluşturur ve ekler."
type: docs
weight: 4000
url: /tr/cpp/aspose.words.tables/cell/ensureminimum/
---
## Cell::EnsureMinimum method


Son çocuk bir paragraf değilse, boş bir paragraf oluşturur ve ekler.

```cpp
void Aspose::Words::Tables::Cell::EnsureMinimum()
```


## Örnekler



Bir hücre düğümünün, içeriğe eklemeye başlamak için ihtiyaç duyduğumuz düğümleri içerdiğini nasıl sağlayacağımızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto table = System::MakeObject<Aspose::Words::Tables::Table>(doc);
doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Tables::Table>>(table);
auto row = System::MakeObject<Aspose::Words::Tables::Row>(doc);
table->AppendChild<System::SharedPtr<Aspose::Words::Tables::Row>>(row);
auto cell = System::MakeObject<Aspose::Words::Tables::Cell>(doc);
row->AppendChild<System::SharedPtr<Aspose::Words::Tables::Cell>>(cell);

// Hücreler, koşular, şekiller ve hatta diğer tablolar gibi tipik öğeler içeren paragraflar içerebilir.
// Yeni hücremizde henüz paragraf bulunmuyor ve koşu ve şekil düğümleri gibi içerikleri ekleyemeyiz.
ASSERT_EQ(0, cell->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());

// Bir hücrede "EnsureMinimum" yöntemini çağırmak, şunun sağlanmasını garantiler
// hücrenin en az bir boş paragrafı olur, ardından içerik ekleyebiliriz.
cell->EnsureMinimum();
cell->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));
```

## Ayrıca Bakınız

* Class [Cell](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
