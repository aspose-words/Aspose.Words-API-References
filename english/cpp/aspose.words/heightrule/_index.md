---
title: Aspose::Words::HeightRule enum
linktitle: HeightRule
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::HeightRule enum. Specifies the rule for determining the height of an object in C++.'
type: docs
weight: 91000
url: /cpp/aspose.words/heightrule/
---
## HeightRule enum


Specifies the rule for determining the height of an object.

```cpp
enum class HeightRule
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| AtLeast | 0 | The height will be at least the specified height in points. It will grow, if needed, to accommodate all text inside an object. |
| Exactly | 1 | The height is specified exactly in points. Please note that if the text cannot fit inside the object of this height, it will appear truncated. |
| Auto | 2 | The height will grow automatically to accommodate all text inside an object. |


## Examples



Shows how to format rows with a document builder. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Row 1, cell 1.");

// Start a second row, and then configure its height. The builder will apply these settings to
// its current row, as well as any new rows it creates afterwards.
builder->EndRow();

System::SharedPtr<Aspose::Words::Tables::RowFormat> rowFormat = builder->get_RowFormat();
rowFormat->set_Height(100);
rowFormat->set_HeightRule(Aspose::Words::HeightRule::Exactly);

builder->InsertCell();
builder->Write(u"Row 2, cell 1.");
builder->EndTable();

// The first row was unaffected by the padding reconfiguration and still holds the default values.
ASPOSE_ASSERT_EQ(0.0, table->get_Rows()->idx_get(0)->get_RowFormat()->get_Height());
ASSERT_EQ(Aspose::Words::HeightRule::Auto, table->get_Rows()->idx_get(0)->get_RowFormat()->get_HeightRule());

ASPOSE_ASSERT_EQ(100.0, table->get_Rows()->idx_get(1)->get_RowFormat()->get_Height());
ASSERT_EQ(Aspose::Words::HeightRule::Exactly, table->get_Rows()->idx_get(1)->get_RowFormat()->get_HeightRule());

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.SetRowFormatting.docx");
```

## See Also

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
