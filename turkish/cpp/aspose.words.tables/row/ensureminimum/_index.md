---
title: "Aspose::Words::Tables::Row::EnsureMinimum yöntemi"
linktitle: "EnsureMinimum"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Tables::Row::EnsureMinimum yöntemi. Row'da hücre yoksa, C++'da bir Cell oluşturur ve ekler."
type: docs
weight: 4000
url: /tr/cpp/aspose.words.tables/row/ensureminimum/
---
## Row::EnsureMinimum method


Eğer [Row](../) içinde hücre yoksa, bir [Cell](../../cell/) oluşturur ve ekler.

```cpp
void Aspose::Words::Tables::Row::EnsureMinimum()
```


## Örnekler



Bir row düğümünün içeri eklemeye başlamamız için gereken düğümleri içerdiğini nasıl sağlayacağımızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto table = System::MakeObject<Aspose::Words::Tables::Table>(doc);
doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Tables::Table>>(table);
auto row = System::MakeObject<Aspose::Words::Tables::Row>(doc);
table->AppendChild<System::SharedPtr<Aspose::Words::Tables::Row>>(row);

// Satırlar hücreler içerir; hücreler ise koşular, şekiller ve hatta diğer tablolar gibi tipik öğeler içeren paragraflar barındırır.
// Yeni satırımız bu düğümlerden hiçbirine sahip değil ve bunlar oluşana kadar içerik ekleyemeyiz.
ASSERT_EQ(0, row->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());

// Bir tablo üzerinde "EnsureMinimum" yöntemini çağırmak, şunun sağlanmasını garantiler
// Tablonun en az bir boş paragraf içeren hücresi vardır.
row->EnsureMinimum();
row->get_FirstCell()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));
```

## Ayrıca Bakınız

* Class [Row](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
