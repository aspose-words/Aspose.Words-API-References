---
title: "Aspose::Words::Drawing::Charts::Chart::get_SourceFullName metodo"
linktitle: "get_SourceFullName"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Drawing::Charts::Chart::get_SourceFullName. Ottiene il percorso e il nome di un file xls/xlsx a cui questo grafico è collegato in C++."
type: docs
weight: 7000
url: /it/cpp/aspose.words.drawing.charts/chart/get_sourcefullname/
---
## Chart::get_SourceFullName method


Ottiene il percorso e il nome di un file xls/xlsx a cui questo grafico è collegato.

```cpp
System::String Aspose::Words::Drawing::Charts::Chart::get_SourceFullName()
```


## Esempi



Mostra come ottenere/impostare il nome completo del documento xls/xlsx esterno se il grafico è collegato.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shape with linked chart.docx");

auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

System::String sourceFullName = shape->get_Chart()->get_SourceFullName();
ASSERT_TRUE(sourceFullName.Contains(u"Examples\\Data\\Spreadsheet.xlsx"));
```

## Vedi anche

* Class [Chart](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
