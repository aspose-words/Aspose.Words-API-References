---
title: "Aspose::Words::DocumentBuilder::InsertChart méthode"
linktitle: "InsertChart"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::DocumentBuilder::InsertChart. Insère un objet graphique dans le document et le redimensionne à la taille spécifiée en C++."
type: docs
weight: 30000
url: /fr/cpp/aspose.words/documentbuilder/insertchart/
---
## DocumentBuilder::InsertChart(Aspose::Words::Drawing::Charts::ChartType, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) method


Insère un objet de graphique dans le document et le redimensionne à la taille spécifiée.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertChart(Aspose::Words::Drawing::Charts::ChartType chartType, Aspose::Words::Drawing::RelativeHorizontalPosition horzPos, double left, Aspose::Words::Drawing::RelativeVerticalPosition vertPos, double top, double width, double height, Aspose::Words::Drawing::WrapType wrapType)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| chartType | Aspose::Words::Drawing::Charts::ChartType | Le type de graphique à insérer dans le document. |
| horzPos | Aspose::Words::Drawing::RelativeHorizontalPosition | Spécifie le point de référence à partir duquel la distance à l’image est mesurée. |
| left | double | Distance en points entre l’origine et le côté gauche de l’image. |
| vertPos | Aspose::Words::Drawing::RelativeVerticalPosition | Spécifie le point de référence à partir duquel la distance à l’image est mesurée. |
| top | double | Distance en points entre l’origine et le côté supérieur de l’image. |
| largeur | double | La largeur de l’image en points. Peut être une valeur négative ou zéro pour demander une échelle de 100 %. |
| hauteur | double | La hauteur de l’image en points. Peut être une valeur négative ou zéro pour demander une échelle de 100 %. |
| wrapType | Aspose::Words::Drawing::WrapType | Spécifie comment le texte s’enroule autour de l’image. |

### ReturnValue

Le nœud d’image qui vient d’être inséré.
## Remarques


Vous pouvez modifier la taille, l’emplacement, la méthode de positionnement et d’autres paramètres de l’image en utilisant l’objet [Shape](../../../aspose.words.drawing/shape/) retourné par cette méthode.

## Exemples



Montre comment spécifier la position et l’habillage lors de l’insertion d’un graphique.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Pie, Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 100, 200, 100, Aspose::Words::Drawing::WrapType::Square);

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertedChartRelativePosition.docx");
```

## Voir aussi

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [ChartType](../../../aspose.words.drawing.charts/charttype/)
* Enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* Enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* Enum [WrapType](../../../aspose.words.drawing/wraptype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertChart(Aspose::Words::Drawing::Charts::ChartType, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType, Aspose::Words::Drawing::Charts::ChartStyle) method


Insère un objet de graphique dans le document et le redimensionne à la taille spécifiée.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertChart(Aspose::Words::Drawing::Charts::ChartType chartType, Aspose::Words::Drawing::RelativeHorizontalPosition horzPos, double left, Aspose::Words::Drawing::RelativeVerticalPosition vertPos, double top, double width, double height, Aspose::Words::Drawing::WrapType wrapType, Aspose::Words::Drawing::Charts::ChartStyle chartStyle)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| chartType | Aspose::Words::Drawing::Charts::ChartType | Le type de graphique à insérer dans le document. |
| horzPos | Aspose::Words::Drawing::RelativeHorizontalPosition | Spécifie le point de référence à partir duquel la distance à l’image est mesurée. |
| left | double | Distance en points entre l’origine et le côté gauche de l’image. |
| vertPos | Aspose::Words::Drawing::RelativeVerticalPosition | Spécifie le point de référence à partir duquel la distance à l’image est mesurée. |
| top | double | Distance en points entre l’origine et le côté supérieur de l’image. |
| largeur | double | La largeur de l’image en points. Peut être une valeur négative ou zéro pour demander une échelle de 100 %. |
| hauteur | double | La hauteur de l’image en points. Peut être une valeur négative ou zéro pour demander une échelle de 100 %. |
| wrapType | Aspose::Words::Drawing::WrapType | Spécifie comment le texte s’enroule autour de l’image. |
| chartStyle | Aspose::Words::Drawing::Charts::ChartStyle | Le style du graphique inséré. |

### ReturnValue

Le nœud d’image qui vient d’être inséré.
## Remarques


Vous pouvez modifier la taille, l’emplacement, la méthode de positionnement et d’autres paramètres de l’image en utilisant l’objet [Shape](../../../aspose.words.drawing/shape/) retourné par cette méthode.

## Voir aussi

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


Insère un objet de graphique dans le document et le redimensionne à la taille spécifiée.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertChart(Aspose::Words::Drawing::Charts::ChartType chartType, double width, double height)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| chartType | Aspose::Words::Drawing::Charts::ChartType | Le type de graphique à insérer dans le document. |
| largeur | double | La largeur de l’image en points. Peut être une valeur négative ou zéro pour demander une échelle de 100 %. |
| hauteur | double | La hauteur de l’image en points. Peut être une valeur négative ou zéro pour demander une échelle de 100 %. |

### ReturnValue

Le nœud d’image qui vient d’être inséré.
## Remarques


Vous pouvez modifier la taille, l’emplacement, la méthode de positionnement et d’autres paramètres de l’image en utilisant l’objet [Shape](../../../aspose.words.drawing/shape/) retourné par cette méthode.

## Exemples



Montre comment insérer un diagramme circulaire dans un document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Pie, Aspose::Words::ConvertUtil::PixelToPoint(300), Aspose::Words::ConvertUtil::PixelToPoint(300))->get_Chart();
chart->get_Series()->Clear();
chart->get_Series()->Add(u"My fruit", System::MakeArray<System::String>({u"Apples", u"Bananas", u"Cherries"}), System::MakeArray<double>({1.3, 2.2, 1.5}));

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertPieChart.docx");
```

## Voir aussi

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [ChartType](../../../aspose.words.drawing.charts/charttype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertChart(Aspose::Words::Drawing::Charts::ChartType, double, double, Aspose::Words::Drawing::Charts::ChartStyle) method


Insère un objet de graphique dans le document et le redimensionne à la taille spécifiée.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertChart(Aspose::Words::Drawing::Charts::ChartType chartType, double width, double height, Aspose::Words::Drawing::Charts::ChartStyle chartStyle)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| chartType | Aspose::Words::Drawing::Charts::ChartType | Le type de graphique à insérer dans le document. |
| largeur | double | La largeur de l’image en points. Peut être une valeur négative ou zéro pour demander une échelle de 100 %. |
| hauteur | double | La hauteur de l’image en points. Peut être une valeur négative ou zéro pour demander une échelle de 100 %. |
| chartStyle | Aspose::Words::Drawing::Charts::ChartStyle | Le style du graphique inséré. |

### ReturnValue

Le nœud d’image qui vient d’être inséré.
## Remarques


Vous pouvez modifier la taille, l’emplacement, la méthode de positionnement et d’autres paramètres de l’image en utilisant l’objet [Shape](../../../aspose.words.drawing/shape/) retourné par cette méthode.

## Voir aussi

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [ChartType](../../../aspose.words.drawing.charts/charttype/)
* Enum [ChartStyle](../../../aspose.words.drawing.charts/chartstyle/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
