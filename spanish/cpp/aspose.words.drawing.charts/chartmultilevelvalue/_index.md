---
title: "Aspose::Words::Drawing::Charts::ChartMultilevelValue class"
linktitle: "ChartMultilevelValue"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::Charts::ChartMultilevelValue class. Representa un valor para gráficos que muestran datos multinivel en C++."
type: docs
weight: 14500
url: /es/cpp/aspose.words.drawing.charts/chartmultilevelvalue/
---
## ChartMultilevelValue class


Representa un valor para gráficos que muestran datos multinivel.

```cpp
class ChartMultilevelValue : public System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [ChartMultilevelValue](./chartmultilevelvalue/)(const System::String\&, const System::String\&, const System::String\&) | Inicializa una nueva instancia de esta clase que representa un valor de tres niveles. |
| [ChartMultilevelValue](./chartmultilevelvalue/)(const System::String\&, const System::String\&) | Inicializa una nueva instancia de esta clase que representa un valor de dos niveles. |
| [ChartMultilevelValue](./chartmultilevelvalue/)(const System::String\&) | Inicializa una nueva instancia de esta clase que representa un valor de un solo nivel. |
| [Equals](./equals/)(System::SharedPtr\<System::Object\>) override | Obtiene una bandera que indica si el objeto especificado es igual al objeto de datos multinivel actual. |
| [get_Level1](./get_level1/)() const | Obtiene el nombre del nivel superior del gráfico al que se refiere este valor. |
| [get_Level2](./get_level2/)() const | Obtiene el nombre del nivel intermedio del gráfico al que se refiere este valor. |
| [get_Level3](./get_level3/)() const | Obtiene el nombre del nivel inferior del gráfico al que se refiere este valor. |
| [GetHashCode](./gethashcode/)() const override | Obtiene un código hash para el objeto de datos multinivel actual. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

## Ejemplos



Muestra cómo crear un gráfico de mapa de árbol.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserta un gráfico de mapa de árbol.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Treemap, 450, 280);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
chart->get_Title()->set_Text(u"World Population");

// Eliminar la serie generada por defecto.
chart->get_Series()->Clear();

// Agregar una serie.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = chart->get_Series()->Add(u"Population by Region", System::MakeArray<System::SharedPtr<Aspose::Words::Drawing::Charts::ChartMultilevelValue>>({System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Asia", u"China"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Asia", u"India"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Asia", u"Indonesia"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Asia", u"Pakistan"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Asia", u"Bangladesh"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Asia", u"Japan"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Asia", u"Philippines"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Asia", u"Other"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Africa", u"Nigeria"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Africa", u"Ethiopia"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Africa", u"Egypt"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Africa", u"Other"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Europe", u"Russia"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Europe", u"Germany"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Europe", u"Other"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Latin America", u"Brazil"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Latin America", u"Mexico"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Latin America", u"Other"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Northern America", u"United States", u"Other"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Northern America", u"Other"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Oceania")}), System::MakeArray<double>({1409670000, 1400744000, 279118866, 241499431, 169828911, 123930000, 112892781, 764000000, 223800000, 107334000, 105914499, 903000000, 146150789, 84607016, 516000000, 203080756, 129713690, 310000000, 335893238, 35000000, 42000000}));

// Mostrar etiquetas de datos.
series->set_HasDataLabels(true);
series->get_DataLabels()->set_ShowValue(true);
series->get_DataLabels()->set_ShowCategoryName(true);
System::String thousandSeparator = System::Globalization::CultureInfo::get_CurrentCulture()->get_NumberFormat()->get_CurrencyGroupSeparator();
series->get_DataLabels()->get_NumberFormat()->set_FormatCode(System::String::Format(u"#{0}0", thousandSeparator));

doc->Save(get_ArtifactsDir() + u"Charts.Treemap.docx");
```

## Ver también

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
