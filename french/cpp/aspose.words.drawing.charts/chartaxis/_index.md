---
title: "Classe Aspose::Words::Drawing::Charts::ChartAxis"
linktitle: "ChartAxis"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Classe Aspose::Words::Drawing::Charts::ChartAxis. Représente les options d'axe du graphique. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 5000
url: /fr/cpp/aspose.words.drawing.charts/chartaxis/
---
## ChartAxis class


Représente les options d'axe du graphique. Pour en savoir plus, consultez l'article de documentation [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/).

```cpp
class ChartAxis : public Aspose::Words::Drawing::Charts::Core::IDmlChartTitleHolder,
                  public Aspose::Words::Drawing::Core::Dml::IDmlExtensionListSource,
                  public Aspose::Words::Drawing::Charts::Core::INumberFormatProvider,
                  public Aspose::Words::Drawing::Charts::Core::IChartFormatSource
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [get_AxisBetweenCategories](./get_axisbetweencategories/)() | Obtient ou définit un indicateur indiquant si l'axe des valeurs croise l'axe des catégories entre les catégories. |
| [get_BaseTimeUnit](./get_basetimeunit/)() | Obtient ou définit la plus petite unité de temps représentée sur l'axe des catégories temporelles. |
| [get_CategoryType](./get_categorytype/)() | Obtient ou définit le type de l'axe des catégories. |
| [get_Crosses](./get_crosses/)() | Spécifie comment cet axe croise l'axe perpendiculaire. |
| [get_CrossesAt](./get_crossesat/)() | Spécifie où sur l'axe perpendiculaire l'axe croise. |
| [get_DisplayUnit](./get_displayunit/)() | Spécifie la valeur d'échelle des unités d'affichage pour l'axe des valeurs. |
| [get_Document](./get_document/)() | Renvoie le document contenant le graphique parent. |
| [get_Format](./get_format/)() | Fournit l'accès au formatage des lignes de l'axe et au remplissage des étiquettes de graduation. |
| [get_HasMajorGridlines](./get_hasmajorgridlines/)() | Obtient ou définit un indicateur indiquant si l'axe possède des quadrillages majeurs. |
| [get_HasMinorGridlines](./get_hasminorgridlines/)() | Obtient ou définit un indicateur indiquant si l'axe possède des quadrillages mineurs. |
| [get_Hidden](./get_hidden/)() | Obtient ou définit un indicateur indiquant si cet axe est masqué ou non. |
| [get_MajorTickMark](./get_majortickmark/)() | Obtient ou définit les marques de graduation majeures. |
| [get_MajorUnit](./get_majorunit/)() | Obtient ou définit la distance entre les marques de graduation majeures. |
| [get_MajorUnitIsAuto](./get_majorunitisauto/)() | Obtient ou définit un indicateur indiquant si la distance par défaut entre les marques de graduation majeures doit être utilisée. |
| [get_MajorUnitScale](./get_majorunitscale/)() | Obtient ou définit la valeur d'échelle pour les marques de graduation majeures sur l'axe des catégories temporelles. |
| [get_MinorTickMark](./get_minortickmark/)() | Obtient ou définit les marques de graduation mineures pour l'axe. |
| [get_MinorUnit](./get_minorunit/)() | Obtient ou définit la distance entre les marques de graduation mineures. |
| [get_MinorUnitIsAuto](./get_minorunitisauto/)() | Obtient ou définit un indicateur indiquant si la distance par défaut entre les marques de graduation mineures doit être utilisée. |
| [get_MinorUnitScale](./get_minorunitscale/)() | Obtient ou définit la valeur d'échelle pour les marques de graduation mineures sur l'axe des catégories temporelles. |
| [get_NumberFormat](./get_numberformat/)() | Renvoie un objet [ChartNumberFormat](../chartnumberformat/) qui permet de définir les formats numériques pour l'axe. |
| [get_ReverseOrder](./get_reverseorder/)() | Obtient ou définit un indicateur indiquant si les valeurs de l'axe doivent être affichées dans l'ordre inverse, c.-à-d. du maximum au minimum. |
| [get_Scaling](./get_scaling/)() | Fournit l'accès aux options de mise à l'échelle de l'axe. |
| [get_TickLabels](./get_ticklabels/)() | Fournit l'accès aux propriétés des étiquettes de marques de graduation de l'axe. |
| [get_TickMarkSpacing](./get_tickmarkspacing/)() | Obtient ou définit l'intervalle auquel les marques de graduation sont dessinées. |
| [get_Title](./get_title/)() | Fournit l'accès aux propriétés du titre de l'axe. |
| [get_Type](./get_type/)() const | Renvoie le type de l'axe. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AxisBetweenCategories](./set_axisbetweencategories/)(bool) | Définisseur pour [Aspose::Words::Drawing::Charts::ChartAxis::get_AxisBetweenCategories](./get_axisbetweencategories/). |
| [set_BaseTimeUnit](./set_basetimeunit/)(Aspose::Words::Drawing::Charts::AxisTimeUnit) | Définisseur pour [Aspose::Words::Drawing::Charts::ChartAxis::get_BaseTimeUnit](./get_basetimeunit/). |
| [set_CategoryType](./set_categorytype/)(Aspose::Words::Drawing::Charts::AxisCategoryType) | Définisseur pour [Aspose::Words::Drawing::Charts::ChartAxis::get_CategoryType](./get_categorytype/). |
| [set_Crosses](./set_crosses/)(Aspose::Words::Drawing::Charts::AxisCrosses) | Définisseur pour [Aspose::Words::Drawing::Charts::ChartAxis::get_Crosses](./get_crosses/). |
| [set_CrossesAt](./set_crossesat/)(double) | Définisseur pour [Aspose::Words::Drawing::Charts::ChartAxis::get_CrossesAt](./get_crossesat/). |
| [set_HasMajorGridlines](./set_hasmajorgridlines/)(bool) | Définisseur pour [Aspose::Words::Drawing::Charts::ChartAxis::get_HasMajorGridlines](./get_hasmajorgridlines/). |
| [set_HasMinorGridlines](./set_hasminorgridlines/)(bool) | Définisseur pour [Aspose::Words::Drawing::Charts::ChartAxis::get_HasMinorGridlines](./get_hasminorgridlines/). |
| [set_Hidden](./set_hidden/)(bool) | Définisseur pour [Aspose::Words::Drawing::Charts::ChartAxis::get_Hidden](./get_hidden/). |
| [set_MajorTickMark](./set_majortickmark/)(Aspose::Words::Drawing::Charts::AxisTickMark) | Définisseur pour [Aspose::Words::Drawing::Charts::ChartAxis::get_MajorTickMark](./get_majortickmark/). |
| [set_MajorUnit](./set_majorunit/)(double) | Définisseur pour [Aspose::Words::Drawing::Charts::ChartAxis::get_MajorUnit](./get_majorunit/). |
| [set_MajorUnitIsAuto](./set_majorunitisauto/)(bool) | Définisseur pour [Aspose::Words::Drawing::Charts::ChartAxis::get_MajorUnitIsAuto](./get_majorunitisauto/). |
| [set_MajorUnitScale](./set_majorunitscale/)(Aspose::Words::Drawing::Charts::AxisTimeUnit) | Définisseur pour [Aspose::Words::Drawing::Charts::ChartAxis::get_MajorUnitScale](./get_majorunitscale/). |
| [set_MinorTickMark](./set_minortickmark/)(Aspose::Words::Drawing::Charts::AxisTickMark) | Définisseur pour [Aspose::Words::Drawing::Charts::ChartAxis::get_MinorTickMark](./get_minortickmark/). |
| [set_MinorUnit](./set_minorunit/)(double) | Définisseur pour [Aspose::Words::Drawing::Charts::ChartAxis::get_MinorUnit](./get_minorunit/). |
| [set_MinorUnitIsAuto](./set_minorunitisauto/)(bool) | Définisseur pour [Aspose::Words::Drawing::Charts::ChartAxis::get_MinorUnitIsAuto](./get_minorunitisauto/). |
| [set_MinorUnitScale](./set_minorunitscale/)(Aspose::Words::Drawing::Charts::AxisTimeUnit) | Définisseur pour [Aspose::Words::Drawing::Charts::ChartAxis::get_MinorUnitScale](./get_minorunitscale/). |
| [set_ReverseOrder](./set_reverseorder/)(bool) | Définisseur pour [Aspose::Words::Drawing::Charts::ChartAxis::get_ReverseOrder](./get_reverseorder/). |
| [set_TickMarkSpacing](./set_tickmarkspacing/)(int32_t) | Définisseur pour [Aspose::Words::Drawing::Charts::ChartAxis::get_TickMarkSpacing](./get_tickmarkspacing/). |
| static [Type](./type/)() |  |

## Exemples



Montre comment insérer un graphique et modifier l'apparence de ses axes.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 500, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

// Effacez la série de données de démonstration du graphique pour commencer avec un graphique vierge.
chart->get_Series()->Clear();

// Insérez une série de graphique avec des catégories pour l'axe X et les valeurs numériques respectives pour l'axe Y.
chart->get_Series()->Add(u"Aspose Test Series", System::MakeArray<System::String>({u"Word", u"PDF", u"Excel", u"GoogleDocs", u"Note"}), System::MakeArray<double>({640, 320, 280, 120, 150}));

// Les axes du graphique offrent diverses options qui peuvent modifier leur apparence,
// telles que leur direction, les graduations principales/secondaires, et les marques de graduation.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartAxis> xAxis = chart->get_AxisX();
xAxis->set_CategoryType(Aspose::Words::Drawing::Charts::AxisCategoryType::Category);
xAxis->set_Crosses(Aspose::Words::Drawing::Charts::AxisCrosses::Minimum);
xAxis->set_ReverseOrder(false);
xAxis->set_MajorTickMark(Aspose::Words::Drawing::Charts::AxisTickMark::Inside);
xAxis->set_MinorTickMark(Aspose::Words::Drawing::Charts::AxisTickMark::Cross);
xAxis->set_MajorUnit(10.0);
xAxis->set_MinorUnit(15.0);
xAxis->get_TickLabels()->set_Offset(50);
xAxis->get_TickLabels()->set_Position(Aspose::Words::Drawing::Charts::AxisTickLabelPosition::Low);
xAxis->get_TickLabels()->set_IsAutoSpacing(false);
xAxis->set_TickMarkSpacing(1);

ASPOSE_ASSERT_EQ(doc, xAxis->get_Document());

System::SharedPtr<Aspose::Words::Drawing::Charts::ChartAxis> yAxis = chart->get_AxisY();
yAxis->set_CategoryType(Aspose::Words::Drawing::Charts::AxisCategoryType::Automatic);
yAxis->set_Crosses(Aspose::Words::Drawing::Charts::AxisCrosses::Maximum);
yAxis->set_ReverseOrder(true);
yAxis->set_MajorTickMark(Aspose::Words::Drawing::Charts::AxisTickMark::Inside);
yAxis->set_MinorTickMark(Aspose::Words::Drawing::Charts::AxisTickMark::Cross);
yAxis->set_MajorUnit(100.0);
yAxis->set_MinorUnit(20.0);
yAxis->get_TickLabels()->set_Position(Aspose::Words::Drawing::Charts::AxisTickLabelPosition::NextToAxis);
yAxis->get_TickLabels()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);
yAxis->get_TickLabels()->get_Font()->set_Color(System::Drawing::Color::get_Red());
yAxis->get_TickLabels()->set_Spacing(1);

// Les graphiques en colonnes n'ont pas d'axe Z.
ASSERT_TRUE(System::TestTools::IsNull(chart->get_AxisZ()));

doc->Save(get_ArtifactsDir() + u"Charts.AxisProperties.docx");
```

## Voir aussi

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
