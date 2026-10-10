---
title: "Aspose::Words::Drawing::Charts::Chart::get_SourceFullName yöntemi"
linktitle: "get_SourceFullName"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::Charts::Chart::get_SourceFullName yöntemi. Bu grafiğin bağlı olduğu xls/xlsx dosyasının yolunu ve adını C++'da alır."
type: docs
weight: 7000
url: /tr/cpp/aspose.words.drawing.charts/chart/get_sourcefullname/
---
## Chart::get_SourceFullName method


Bu çizelgenin bağlı olduğu xls/xlsx dosyasının yolunu ve adını alır.

```cpp
System::String Aspose::Words::Drawing::Charts::Chart::get_SourceFullName()
```


## Örnekler



Grafik bağlıysa dış xls/xlsx belgesinin tam adını almayı/ayarlamayı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shape with linked chart.docx");

auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

System::String sourceFullName = shape->get_Chart()->get_SourceFullName();
ASSERT_TRUE(sourceFullName.Contains(u"Examples\\Data\\Spreadsheet.xlsx"));
```

## Ayrıca Bakınız

* Class [Chart](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
