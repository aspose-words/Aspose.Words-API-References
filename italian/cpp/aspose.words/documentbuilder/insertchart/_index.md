---
title: "Aspose::Words::DocumentBuilder::InsertChart method"
linktitle: "InsertChart"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::DocumentBuilder::InsertChart. Inserisce un oggetto grafico nel documento e lo scala alla dimensione specificata in C++."
type: docs
weight: 30000
url: /it/cpp/aspose.words/documentbuilder/insertchart/
---
## DocumentBuilder::InsertChart(Aspose::Words::Drawing::Charts::ChartType, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) method


Inserisce un oggetto grafico nel documento e lo scala alla dimensione specificata.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertChart(Aspose::Words::Drawing::Charts::ChartType chartType, Aspose::Words::Drawing::RelativeHorizontalPosition horzPos, double left, Aspose::Words::Drawing::RelativeVerticalPosition vertPos, double top, double width, double height, Aspose::Words::Drawing::WrapType wrapType)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| chartType | Aspose::Words::Drawing::Charts::ChartType | Il tipo di grafico da inserire nel documento. |
| horzPos | Aspose::Words::Drawing::RelativeHorizontalPosition | Specifica da dove viene misurata la distanza dall'immagine. |
| left | double | Distanza in punti dall'origine al lato sinistro dell'immagine. |
| vertPos | Aspose::Words::Drawing::RelativeVerticalPosition | Specifica da dove viene misurata la distanza dall'immagine. |
| superiore | double | Distanza in punti dall'origine al lato superiore dell'immagine. |
| larghezza | double | La larghezza dell'immagine in punti. Può essere un valore negativo o zero per richiedere una scala del 100%. |
| altezza | double | L'altezza dell'immagine in punti. Può essere un valore negativo o zero per richiedere una scala del 100%. |
| wrapType | Aspose::Words::Drawing::WrapType | Specifica come avvolgere il testo attorno all'immagine. |

### ReturnValue

Il nodo immagine appena inserito.
## Note


Puoi modificare le dimensioni, la posizione, il metodo di posizionamento dell'immagine e altre impostazioni usando l'oggetto [Shape](../../../aspose.words.drawing/shape/) restituito da questo metodo.

## Esempi



Mostra come specificare posizione e avvolgimento durante l'inserimento di un grafico.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Pie, Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 100, 200, 100, Aspose::Words::Drawing::WrapType::Square);

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertedChartRelativePosition.docx");
```

## Vedi anche

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [ChartType](../../../aspose.words.drawing.charts/charttype/)
* Enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* Enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* Enum [WrapType](../../../aspose.words.drawing/wraptype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertChart(Aspose::Words::Drawing::Charts::ChartType, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType, Aspose::Words::Drawing::Charts::ChartStyle) method


Inserisce un oggetto grafico nel documento e lo scala alla dimensione specificata.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertChart(Aspose::Words::Drawing::Charts::ChartType chartType, Aspose::Words::Drawing::RelativeHorizontalPosition horzPos, double left, Aspose::Words::Drawing::RelativeVerticalPosition vertPos, double top, double width, double height, Aspose::Words::Drawing::WrapType wrapType, Aspose::Words::Drawing::Charts::ChartStyle chartStyle)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| chartType | Aspose::Words::Drawing::Charts::ChartType | Il tipo di grafico da inserire nel documento. |
| horzPos | Aspose::Words::Drawing::RelativeHorizontalPosition | Specifica da dove viene misurata la distanza dall'immagine. |
| left | double | Distanza in punti dall'origine al lato sinistro dell'immagine. |
| vertPos | Aspose::Words::Drawing::RelativeVerticalPosition | Specifica da dove viene misurata la distanza dall'immagine. |
| superiore | double | Distanza in punti dall'origine al lato superiore dell'immagine. |
| larghezza | double | La larghezza dell'immagine in punti. Può essere un valore negativo o zero per richiedere una scala del 100%. |
| altezza | double | L'altezza dell'immagine in punti. Può essere un valore negativo o zero per richiedere una scala del 100%. |
| wrapType | Aspose::Words::Drawing::WrapType | Specifica come avvolgere il testo attorno all'immagine. |
| chartStyle | Aspose::Words::Drawing::Charts::ChartStyle | Lo stile del grafico inserito. |

### ReturnValue

Il nodo immagine appena inserito.
## Note


Puoi modificare le dimensioni, la posizione, il metodo di posizionamento dell'immagine e altre impostazioni usando l'oggetto [Shape](../../../aspose.words.drawing/shape/) restituito da questo metodo.

## Vedi anche

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [ChartType](../../../aspose.words.drawing.charts/charttype/)
* Enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* Enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* Enum [WrapType](../../../aspose.words.drawing/wraptype/)
* Enum [ChartStyle](../../../aspose.words.drawing.charts/chartstyle/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertChart(Aspose::Words::Drawing::Charts::ChartType, double, double) method


Inserisce un oggetto grafico nel documento e lo scala alla dimensione specificata.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertChart(Aspose::Words::Drawing::Charts::ChartType chartType, double width, double height)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| chartType | Aspose::Words::Drawing::Charts::ChartType | Il tipo di grafico da inserire nel documento. |
| larghezza | double | La larghezza dell'immagine in punti. Può essere un valore negativo o zero per richiedere una scala del 100%. |
| altezza | double | L'altezza dell'immagine in punti. Può essere un valore negativo o zero per richiedere una scala del 100%. |

### ReturnValue

Il nodo immagine appena inserito.
## Note


Puoi modificare le dimensioni, la posizione, il metodo di posizionamento dell'immagine e altre impostazioni usando l'oggetto [Shape](../../../aspose.words.drawing/shape/) restituito da questo metodo.

## Esempi



Mostra come inserire un grafico a torta in un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Pie, Aspose::Words::ConvertUtil::PixelToPoint(300), Aspose::Words::ConvertUtil::PixelToPoint(300))->get_Chart();
chart->get_Series()->Clear();
chart->get_Series()->Add(u"My fruit", System::MakeArray<System::String>({u"Apples", u"Bananas", u"Cherries"}), System::MakeArray<double>({1.3, 2.2, 1.5}));

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertPieChart.docx");
```

## Vedi anche

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [ChartType](../../../aspose.words.drawing.charts/charttype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertChart(Aspose::Words::Drawing::Charts::ChartType, double, double, Aspose::Words::Drawing::Charts::ChartStyle) method


Inserisce un oggetto grafico nel documento e lo scala alla dimensione specificata.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertChart(Aspose::Words::Drawing::Charts::ChartType chartType, double width, double height, Aspose::Words::Drawing::Charts::ChartStyle chartStyle)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| chartType | Aspose::Words::Drawing::Charts::ChartType | Il tipo di grafico da inserire nel documento. |
| larghezza | double | La larghezza dell'immagine in punti. Può essere un valore negativo o zero per richiedere una scala del 100%. |
| altezza | double | L'altezza dell'immagine in punti. Può essere un valore negativo o zero per richiedere una scala del 100%. |
| chartStyle | Aspose::Words::Drawing::Charts::ChartStyle | Lo stile del grafico inserito. |

### ReturnValue

Il nodo immagine appena inserito.
## Note


Puoi modificare le dimensioni, la posizione, il metodo di posizionamento dell'immagine e altre impostazioni usando l'oggetto [Shape](../../../aspose.words.drawing/shape/) restituito da questo metodo.

## Vedi anche

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [ChartType](../../../aspose.words.drawing.charts/charttype/)
* Enum [ChartStyle](../../../aspose.words.drawing.charts/chartstyle/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
