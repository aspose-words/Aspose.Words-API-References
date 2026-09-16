---
title: "Aspose::Words::Tables::Row::get_Hidden 方法"
linktitle: "get_Hidden"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Tables::Row::get_Hidden 方法。获取或设置一个标志，指示此行在 C++ 中是否隐藏。"
type: docs
weight: 6500
url: /zh/cpp/aspose.words.tables/row/get_hidden/
---
## Row::get_Hidden method


获取或设置指示此行是否隐藏的标志。

```cpp
bool Aspose::Words::Tables::Row::get_Hidden()
```


## 示例



展示如何隐藏表格行。
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

## 另见

* Class [Row](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
