---
title: "Aspose::Words::NodeCollection::IndexOf yöntemi"
linktitle: "IndexOf"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::NodeCollection::IndexOf yöntemi. Belirtilen düğümün C++'ta sıfır tabanlı indeksini döndürür."
type: docs
weight: 9000
url: /tr/cpp/aspose.words/nodecollection/indexof/
---
## NodeCollection::IndexOf method


Belirtilen düğümün sıfır tabanlı indeksini döndürür.

```cpp
int32_t Aspose::Words::NodeCollection::IndexOf(const System::SharedPtr<Aspose::Words::Node> &node)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| düğüm | const System::SharedPtr\<Aspose::Words::Node\>\& | Bulunacak düğüm. |

### ReturnValue

Düğümün koleksiyon içindeki sıfır tabanlı indeksi, bulunursa; aksi takdirde -1.
## Açıklamalar


Bu yöntem lineer arama yapar; bu nedenle ortalama yürütme süresi [Count](../get_count/) ile orantılıdır.

## Örnekler



Bir koleksiyondaki bir düğümün indeksini nasıl alacağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");

System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);
System::SharedPtr<Aspose::Words::NodeCollection> allTables = doc->GetChildNodes(Aspose::Words::NodeType::Table, true);

ASSERT_EQ(0, allTables->IndexOf(table));

System::SharedPtr<Aspose::Words::Tables::Row> row = table->get_Rows()->idx_get(2);

ASSERT_EQ(2, table->IndexOf(row));

System::SharedPtr<Aspose::Words::Tables::Cell> cell = row->get_LastCell();

ASSERT_EQ(4, row->IndexOf(cell));
```

## Ayrıca Bakınız

* Class [Node](../../node/)
* Class [NodeCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
