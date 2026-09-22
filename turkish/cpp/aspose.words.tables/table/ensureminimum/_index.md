---
title: "Aspose::Words::Tables::Table::EnsureMinimum yöntemi"
linktitle: "EnsureMinimum"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Tables::Table::EnsureMinimum yöntemi. Tablo satıra sahip değilse, C++'ta bir Row oluşturur ve ekler."
type: docs
weight: 8000
url: /tr/cpp/aspose.words.tables/table/ensureminimum/
---
## Table::EnsureMinimum method


Tablo satıra sahip değilse, bir [Row](../../row/) oluşturur ve ekler.

```cpp
void Aspose::Words::Tables::Table::EnsureMinimum()
```


## Örnekler



Bir tablo düğümünün içerik eklemek için ihtiyaç duyduğumuz düğümleri içerdiğinden nasıl emin olunacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto table = System::MakeObject<Aspose::Words::Tables::Table>(doc);
doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Tables::Table>>(table);

// Tablolar satırları, satırlar hücreleri, hücreler ise paragrafları içerir
// koşular, şekiller ve hatta diğer tablolar gibi tipik öğelerle.
// Yeni tablomuz bu düğümlerden hiçbirine sahip değil ve bunlar oluşana kadar içerik ekleyemeyiz.
ASSERT_EQ(0, table->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());

// Bir tablo üzerinde "EnsureMinimum" yöntemini çağırmak, şunun sağlanmasını garantiler
// Tablonun en az bir satırı ve boş bir paragraf içeren bir hücresi vardır.
table->EnsureMinimum();
table->get_FirstRow()->get_FirstCell()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));
```

## Ayrıca Bakınız

* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
