---
title: "Aspose::Words::Tables::TableCollection sınıfı"
linktitle: "TableCollection"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Tables::TableCollection sınıfı. Table düğümlerinin bir koleksiyonuna tipli erişim sağlar. Daha fazla bilgi için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 9000
url: /tr/cpp/aspose.words.tables/tablecollection/
---
## TableCollection class


Bir koleksiyon içindeki [Table](../table/) düğümlerine tipli erişim sağlar. Daha fazla bilgi için [Working with Tables](https://docs.aspose.com/words/cpp/working-with-tables/) belge makalesini ziyaret edin.

```cpp
class TableCollection : public Aspose::Words::NodeCollection
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [Add](../../aspose.words/nodecollection/add/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Bir düğümü koleksiyonun sonuna ekler. |
| [Clear](../../aspose.words/nodecollection/clear/)() | Bu koleksiyondaki ve belgedeki tüm düğümleri kaldırır. |
| [Contains](../../aspose.words/nodecollection/contains/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Bir düğümün koleksiyonda olup olmadığını belirler. |
| [get_Count](../../aspose.words/nodecollection/get_count/)() | Koleksiyondaki düğüm sayısını alır. |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator/)() override | Düğümlerin koleksiyonu üzerinde basit bir "foreach" tarzı yineleme sağlar. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Verilen indeksteki bir [Table](../table/) alır. |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Belirtilen düğümün sıfır tabanlı indeksini döndürür. |
| [Insert](../../aspose.words/nodecollection/insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Node\>\&) | Belirtilen indeksde bir düğümü koleksiyona ekler. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](../../aspose.words/nodecollection/remove/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Düğümü koleksiyondan ve belgeden kaldırır. |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(int32_t) | Belirtilen indeksteki düğümü koleksiyondan ve belgeden kaldırır. |
| [ToArray](./toarray/)() | Koleksiyondaki tüm tabloları yeni bir tablo dizisine kopyalar. |
| static [Type](./type/)() |  |

## Örnekler



Bir belgedeki tüm tabloların ilk ve son satırlarını nasıl kaldıracağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");

System::SharedPtr<Aspose::Words::Tables::TableCollection> tables = doc->get_FirstSection()->get_Body()->get_Tables();

ASSERT_EQ(5, tables->idx_get(0)->get_Rows()->get_Count());
ASSERT_EQ(4, tables->idx_get(1)->get_Rows()->get_Count());

for (auto&& table : System::IterateOver(tables->LINQ_OfType<System::SharedPtr<Aspose::Words::Tables::Table> >()))
{
    System::SharedPtr<Aspose::Words::Tables::Row> condExpression = table->get_FirstRow();
    if (condExpression != nullptr)
    {
        condExpression->Remove();
    }
    System::SharedPtr<Aspose::Words::Tables::Row> condExpression2 = table->get_LastRow();
    if (condExpression2 != nullptr)
    {
        condExpression2->Remove();
    }
}

ASSERT_EQ(3, tables->idx_get(0)->get_Rows()->get_Count());
ASSERT_EQ(2, tables->idx_get(1)->get_Rows()->get_Count());
```

## Ayrıca Bakınız

* Class [NodeCollection](../../aspose.words/nodecollection/)
* Namespace [Aspose::Words::Tables](../)
* Library [Aspose.Words for C++](../../)
