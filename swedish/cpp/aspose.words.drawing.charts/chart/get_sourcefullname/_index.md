---
title: "Aspose::Words::Drawing::Charts::Chart::get_SourceFullName metod"
linktitle: "get_SourceFullName"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::Charts::Chart::get_SourceFullName metod. Hämtar sökvägen och namnet på en xls/xlsx‑fil som detta diagram är länkat till i C++."
type: docs
weight: 7000
url: /sv/cpp/aspose.words.drawing.charts/chart/get_sourcefullname/
---
## Chart::get_SourceFullName method


Hämtar sökvägen och namnet på en xls/xlsx-fil som detta diagram är länkat till.

```cpp
System::String Aspose::Words::Drawing::Charts::Chart::get_SourceFullName()
```


## Exempel



Visar hur man hämtar/anger det fullständiga namnet på det externa xls/xlsx‑dokumentet om diagrammet är länkat.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shape with linked chart.docx");

auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

System::String sourceFullName = shape->get_Chart()->get_SourceFullName();
ASSERT_TRUE(sourceFullName.Contains(u"Examples\\Data\\Spreadsheet.xlsx"));
```

## Se även

* Class [Chart](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
