---
title: Aspose::Words::Drawing::Charts::Chart::set_SourceFullName method
linktitle: set_SourceFullName
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::Charts::Chart::set_SourceFullName method. Gets the path and name of an xls/xlsx file this chart is linked to in C++.'
type: docs
weight: 11000
url: /cpp/aspose.words.drawing.charts/chart/set_sourcefullname/
---
## Chart::set_SourceFullName method


Gets the path and name of an xls/xlsx file this chart is linked to.

```cpp
void Aspose::Words::Drawing::Charts::Chart::set_SourceFullName(const System::String & value)
```

## Examples


Shows how to get/set the full name of the external xls/xlsx document if the chart is linked.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(System::String(get_MyDir() + u"Shape with linked chart.docx"));

auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(NodeType::Shape, 0, true));

System::String sourceFullName = shape->get_Chart()->get_SourceFullName();
ASSERT_TRUE(sourceFullName.Contains(u"Examples\\Data\\Spreadsheet.xlsx"));
```
## See Also

* Class [Chart](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
