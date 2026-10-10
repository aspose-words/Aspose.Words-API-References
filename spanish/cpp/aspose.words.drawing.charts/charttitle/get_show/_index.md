---
title: "Aspose::Words::Drawing::Charts::ChartTitle::get_Show método"
linktitle: "get_Show"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::Charts::ChartTitle::get_Show método. Determina si el título debe mostrarse para este gráfico. El valor predeterminado es true en C++."
type: docs
weight: 3000
url: /es/cpp/aspose.words.drawing.charts/charttitle/get_show/
---
## ChartTitle::get_Show method


Determina si el título debe mostrarse para este gráfico. El valor predeterminado es **true**.

```cpp
bool Aspose::Words::Drawing::Charts::ChartTitle::get_Show()
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
