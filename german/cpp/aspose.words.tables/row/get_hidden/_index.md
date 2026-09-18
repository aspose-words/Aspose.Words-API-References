---
title: "Aspose::Words::Tables::Row::get_Hidden Methode"
linktitle: "get_Hidden"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Tables::Row::get_Hidden Methode. Gibt ein Flag zurück oder setzt es, das angibt, ob diese Row in C++ ausgeblendet ist oder nicht."
type: docs
weight: 6500
url: /de/cpp/aspose.words.tables/row/get_hidden/
---
## Row::get_Hidden method


Liest oder setzt ein Flag, das angibt, ob diese Zeile ausgeblendet ist oder nicht.

```cpp
bool Aspose::Words::Tables::Row::get_Hidden()
```


## Beispiele



Zeigt, wie man eine Tabellen-Row ausblendet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");

System::SharedPtr<Aspose::Words::Tables::Row> row = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0)->get_FirstRow();
row->set_Hidden(true);

doc->Save(get_ArtifactsDir() + u"Table.HiddenRow.docx");

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Table.HiddenRow.docx");

row = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0)->get_FirstRow();
ASSERT_TRUE(row->get_Hidden());

for (auto&& cell : System::IterateOver<Aspose::Words::Tables::Cell>(row->get_Cells()))
{
    for (auto&& para : System::IterateOver<Aspose::Words::Paragraph>(cell->get_Paragraphs()))
    {
        for (auto&& run : System::IterateOver<Aspose::Words::Run>(para->get_Runs()))
        {
            ASSERT_TRUE(run->get_Font()->get_Hidden());
        }
    }
}
```

## Siehe auch

* Class [Row](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
