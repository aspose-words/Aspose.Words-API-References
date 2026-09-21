---
title: "Aspose::Words::Tables::Row::get_Hidden‑metod"
linktitle: "get_Hidden"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Tables::Row::get_Hidden‑metod. Hämtar eller anger en flagga som visar om denna rad är dold eller inte i C++."
type: docs
weight: 6500
url: /sv/cpp/aspose.words.tables/row/get_hidden/
---
## Row::get_Hidden method


Hämtar eller anger en flagga som visar om den här raden är dold eller inte.

```cpp
bool Aspose::Words::Tables::Row::get_Hidden()
```


## Exempel



Visar hur man döljer en tabellrad.
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

## Se även

* Class [Row](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
