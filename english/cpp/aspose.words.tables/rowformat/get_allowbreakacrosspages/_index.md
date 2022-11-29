---
title: get_AllowBreakAcrossPages
second_title: Aspose.Words for C++ API Reference
description: True if the text in a table row is allowed to split across a page break.
type: docs
weight: 14
url: /cpp/aspose.words.tables/rowformat/get_allowbreakacrosspages/
---
## RowFormat::get_AllowBreakAcrossPages method


True if the text in a table row is allowed to split across a page break.

```cpp
bool Aspose::Words::Tables::RowFormat::get_AllowBreakAcrossPages()
```


## Examples



Shows how to disable rows breaking across pages for every row in a table. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Table spanning two pages.docx");
SharedPtr<Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

// Set the "AllowBreakAcrossPages" property to "false" to keep the row
// in one piece if a table spans two pages, which break up along that row.
// If the row is too big to fit in one page, Microsoft Word will push it down to the next page.
// Set the "AllowBreakAcrossPages" property to "true" to allow the row to break up across two pages.
for (const auto& row : System::IterateOver(table->LINQ_OfType<SharedPtr<Row>>()))
{
    row->get_RowFormat()->set_AllowBreakAcrossPages(allowBreakAcrossPages);
}

doc->Save(ArtifactsDir + u"Table.AllowBreakAcrossPages.docx");
```

## See Also

* Class [RowFormat](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words](../../../)
