---
title: "Aspose::Words::Drawing::Charts::Chart::get_SourceFullName método"
linktitle: "get_SourceFullName"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Drawing::Charts::Chart::get_SourceFullName. Obtiene la ruta y el nombre de un archivo xls/xlsx al que este gráfico está vinculado en C++."
type: docs
weight: 7000
url: /es/cpp/aspose.words.drawing.charts/chart/get_sourcefullname/
---
## Chart::get_SourceFullName method


Obtiene la ruta y el nombre de un archivo xls/xlsx al que está vinculado este gráfico.

```cpp
System::String Aspose::Words::Drawing::Charts::Chart::get_SourceFullName()
```


## Ejemplos



Muestra cómo obtener/establecer el nombre completo del documento xls/xlsx externo si el gráfico está vinculado.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shape with linked chart.docx");

auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

System::String sourceFullName = shape->get_Chart()->get_SourceFullName();
ASSERT_TRUE(sourceFullName.Contains(u"Examples\\Data\\Spreadsheet.xlsx"));
```

## Ver también

* Class [Chart](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
