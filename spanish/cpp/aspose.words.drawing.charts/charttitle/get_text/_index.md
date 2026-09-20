---
title: "Método Aspose::Words::Drawing::Charts::ChartTitle::get_Text"
linktitle: "get_Text"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Drawing::Charts::ChartTitle::get_Text. Obtiene o establece el texto del título del gráfico. Si se especifica un valor nulo o vacío, se mostrará un título generado automáticamente en C++."
type: docs
weight: 4000
url: /es/cpp/aspose.words.drawing.charts/charttitle/get_text/
---
## ChartTitle::get_Text method


Obtiene o establece el texto del título del gráfico. Si el valor es **null** o está vacío, se mostrará un título generado automáticamente.

```cpp
System::String Aspose::Words::Drawing::Charts::ChartTitle::get_Text()
```


## Ejemplos



Muestra cómo insertar un gráfico y establecer un título.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserta una forma de gráfico con un DocumentBuilder y obtén su gráfico.
System::SharedPtr<Aspose::Words::Drawing::Shape> chartShape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Bar, 400, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = chartShape->get_Chart();

// Utiliza la propiedad "Title" para dar a nuestro gráfico un título, que aparece en la parte superior central del área del gráfico.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartTitle> title = chart->get_Title();
title->set_Text(u"My Chart");
title->get_Font()->set_Size(15);
title->get_Font()->set_Color(System::Drawing::Color::get_Blue());

// Establece la propiedad "Show" a "true" para que el título sea visible.
title->set_Show(true);

// Establece la propiedad "Overlay" a "true". Da más espacio a otros elementos del gráfico permitiendo que se superpongan al título.
title->set_Overlay(true);

doc->Save(get_ArtifactsDir() + u"Charts.ChartTitle.docx");
```

## Ver también

* Class [ChartTitle](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
