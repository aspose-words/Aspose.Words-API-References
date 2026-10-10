---
title: "Aspose::Words::Tables::TableCollection class"
linktitle: "TableCollection"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Tables::TableCollection class. Tillhandahåller typad åtkomst till en samling av Table-noder. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 9000
url: /sv/cpp/aspose.words.tables/tablecollection/
---
## TableCollection class


Tillhandahåller typad åtkomst till en samling av [Table](../table/) noder. För att lära dig mer, besök [Working with Tables](https://docs.aspose.com/words/cpp/working-with-tables/) dokumentationsartikel.

```cpp
class TableCollection : public Aspose::Words::NodeCollection
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [Add](../../aspose.words/nodecollection/add/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Lägger till en nod i slutet av samlingen. |
| [Clear](../../aspose.words/nodecollection/clear/)() | Tar bort alla noder från denna samling och från dokumentet. |
| [Contains](../../aspose.words/nodecollection/contains/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Avgör om en nod finns i samlingen. |
| [get_Count](../../aspose.words/nodecollection/get_count/)() | Hämtar antalet noder i samlingen. |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator/)() override | Tillhandahåller en enkel "foreach"‑liknande iteration över samlingen av noder. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Hämtar en [Table](../table/) på det angivna indexet. |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Returnerar det nollbaserade indexet för den angivna noden. |
| [Insert](../../aspose.words/nodecollection/insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Node\>\&) | Infogar en nod i samlingen på det angivna indexet. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](../../aspose.words/nodecollection/remove/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Tar bort noden från samlingen och från dokumentet. |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(int32_t) | Tar bort noden på det angivna indexet från samlingen och från dokumentet. |
| [ToArray](./toarray/)() | Kopierar alla tabeller från samlingen till en ny array av tabeller. |
| static [Type](./type/)() |  |

## Exempel



Visar hur man tar bort den första och sista raden i alla tabeller i ett dokument.
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

## Se även

* Class [NodeCollection](../../aspose.words/nodecollection/)
* Namespace [Aspose::Words::Tables](../)
* Library [Aspose.Words for C++](../../)
