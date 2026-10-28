---
title: Aspose::Words::Tables::Row::set_Hidden method
linktitle: set_Hidden
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Tables::Row::set_Hidden method. Sets a flag indicating whether this row is hidden or not in C++.'
type: docs
weight: 16000
url: /cpp/aspose.words.tables/row/set_hidden/
---
## Row::set_Hidden method


Sets a flag indicating whether this row is hidden or not.

```cpp
void Aspose::Words::Tables::Row::set_Hidden(bool value)
```

## Remarks

 Hidden row is not supported for WordML and ODT documents. 
## Examples


Shows how to hide a table row.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(System::String(get_MyDir() + u"Tables.docx"));

System::SharedPtr<Aspose::Words::Tables::Row> row = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0)->get_FirstRow();
row->set_Hidden(true);

doc->Save(get_ArtifactsDir() + u"Table.HiddenRow.docx");

doc = System::MakeObject<Aspose::Words::Document>(System::String(get_ArtifactsDir() + u"Table.HiddenRow.docx"));

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
## See Also

* Class [Row](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
