---
title: "Aspose::Words::Tables::TableCollection Klasse"
linktitle: "TableCollection"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Tables::TableCollection Klasse. Bietet typisierten Zugriff auf eine Sammlung von Table‑Knoten. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 9000
url: /de/cpp/aspose.words.tables/tablecollection/
---
## TableCollection class


Bietet typisierten Zugriff auf eine Sammlung von [Table](../table/) Knoten. Weitere Informationen finden Sie im Dokumentationsartikel [Working with Tables](https://docs.aspose.com/words/cpp/working-with-tables/).

```cpp
class TableCollection : public Aspose::Words::NodeCollection
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [Add](../../aspose.words/nodecollection/add/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Fügt einen Knoten am Ende der Sammlung hinzu. |
| [Clear](../../aspose.words/nodecollection/clear/)() | Entfernt alle Knoten aus dieser Sammlung und aus dem Dokument. |
| [Contains](../../aspose.words/nodecollection/contains/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Bestimmt, ob ein Knoten in der Sammlung ist. |
| [get_Count](../../aspose.words/nodecollection/get_count/)() | Ermittelt die Anzahl der Knoten in der Sammlung. |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator/)() override | Bietet eine einfache \"foreach\"-artige Iteration über die Sammlung von Knoten. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Ruft ein [Table](../table/) am angegebenen Index ab. |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Gibt den nullbasierten Index des angegebenen Knotens zurück. |
| [Insert](../../aspose.words/nodecollection/insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Node\>\&) | Fügt einen Knoten in die Sammlung am angegebenen Index ein. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](../../aspose.words/nodecollection/remove/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Entfernt den Knoten aus der Sammlung und aus dem Dokument. |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(int32_t) | Entfernt den Knoten am angegebenen Index aus der Sammlung und aus dem Dokument. |
| [ToArray](./toarray/)() | Kopiert alle Tabellen aus der Sammlung in ein neues Array von Tabellen. |
| static [Type](./type/)() |  |

## Beispiele



Zeigt, wie die erste und letzte Zeile aller Tabellen in einem Dokument entfernt werden.
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

## Siehe auch

* Class [NodeCollection](../../aspose.words/nodecollection/)
* Namespace [Aspose::Words::Tables](../)
* Library [Aspose.Words for C++](../../)
