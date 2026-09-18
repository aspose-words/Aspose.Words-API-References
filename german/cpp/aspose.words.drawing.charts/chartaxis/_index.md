---
title: "Aspose::Words::Drawing::Charts::ChartAxis Klasse"
linktitle: "ChartAxis"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::Charts::ChartAxis Klasse. Stellt die Achsenoptionen des Diagramms dar. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 5000
url: /de/cpp/aspose.words.drawing.charts/chartaxis/
---
## ChartAxis class


Stellt die Achsenoptionen des Diagramms dar. Weitere Informationen finden Sie im Dokumentationsartikel [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/).

```cpp
class ChartAxis : public Aspose::Words::Drawing::Charts::Core::IDmlChartTitleHolder,
                  public Aspose::Words::Drawing::Core::Dml::IDmlExtensionListSource,
                  public Aspose::Words::Drawing::Charts::Core::INumberFormatProvider,
                  public Aspose::Words::Drawing::Charts::Core::IChartFormatSource
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get_AxisBetweenCategories](./get_axisbetweencategories/)() | Ermittelt oder legt ein Flag fest, das angibt, ob die Werteachse die Kategorienachse zwischen den Kategorien schneidet. |
| [get_BaseTimeUnit](./get_basetimeunit/)() | Ruft die kleinste Zeiteinheit ab oder legt sie fest, die auf der Zeitkategorienachse dargestellt wird. |
| [get_CategoryType](./get_categorytype/)() | Ermittelt oder legt den Typ der Kategorienachse fest. |
| [get_Crosses](./get_crosses/)() | Gibt an, wie diese Achse die senkrechte Achse schneidet. |
| [get_CrossesAt](./get_crossesat/)() | Gibt an, wo auf der senkrechten Achse die Achse schneidet. |
| [get_DisplayUnit](./get_displayunit/)() | Gibt den Skalierungswert der Anzeigeeinheiten für die Werteachse an. |
| [get_Document](./get_document/)() | Gibt das Dokument zurück, das das übergeordnete Diagramm enthält. |
| [get_Format](./get_format/)() | Bietet Zugriff auf die Linienformatierung der Achse und die Füllung der Achsenbeschriftungen. |
| [get_HasMajorGridlines](./get_hasmajorgridlines/)() | Ermittelt oder legt ein Flag fest, das angibt, ob die Achse Hauptgitternetzlinien hat. |
| [get_HasMinorGridlines](./get_hasminorgridlines/)() | Ermittelt oder legt ein Flag fest, das angibt, ob die Achse Nebengitternetzlinien hat. |
| [get_Hidden](./get_hidden/)() | Ermittelt oder legt ein Flag fest, das angibt, ob diese Achse ausgeblendet ist oder nicht. |
| [get_MajorTickMark](./get_majortickmark/)() | Ruft die Hauptteilstriche ab oder legt sie fest. |
| [get_MajorUnit](./get_majorunit/)() | Ruft den Abstand zwischen den Hauptteilstrichen ab oder legt ihn fest. |
| [get_MajorUnitIsAuto](./get_majorunitisauto/)() | Ermittelt oder legt ein Flag fest, das angibt, ob der Standardabstand zwischen den Hauptteilstrichen verwendet werden soll. |
| [get_MajorUnitScale](./get_majorunitscale/)() | Ruft den Skalierungswert für Hauptteilstriche auf der Zeitkategorienachse ab oder legt ihn fest. |
| [get_MinorTickMark](./get_minortickmark/)() | Ruft die Nebenteilstriche für die Achse ab oder legt sie fest. |
| [get_MinorUnit](./get_minorunit/)() | Ruft den Abstand zwischen den Nebenteilstrichen ab oder legt ihn fest. |
| [get_MinorUnitIsAuto](./get_minorunitisauto/)() | Ermittelt oder legt ein Flag fest, das angibt, ob der Standardabstand zwischen den Nebenteilstrichen verwendet werden soll. |
| [get_MinorUnitScale](./get_minorunitscale/)() | Ruft den Skalierungswert für Nebenteilstriche auf der Zeitkategorienachse ab oder legt ihn fest. |
| [get_NumberFormat](./get_numberformat/)() | Gibt ein [ChartNumberFormat](../chartnumberformat/) Objekt zurück, das die Definition von Zahlenformaten für die Achse ermöglicht. |
| [get_ReverseOrder](./get_reverseorder/)() | Ruft ein Flag ab oder legt es fest, das angibt, ob Achsenwerte in umgekehrter Reihenfolge angezeigt werden sollen, d. h. von Max nach Min. |
| [get_Scaling](./get_scaling/)() | Bietet Zugriff auf die Skalierungsoptionen der Achse. |
| [get_TickLabels](./get_ticklabels/)() | Bietet Zugriff auf die Eigenschaften der Achsen‑Teilstrich‑Beschriftungen. |
| [get_TickMarkSpacing](./get_tickmarkspacing/)() | Liest oder setzt das Intervall, in dem die Tick-Markierungen gezeichnet werden. |
| [get_Title](./get_title/)() | Stellt Zugriff auf die Achsentitel-Eigenschaften bereit. |
| [get_Type](./get_type/)() const | Gibt den Typ der Achse zurück. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AxisBetweenCategories](./set_axisbetweencategories/)(bool) | Setzer für [Aspose::Words::Drawing::Charts::ChartAxis::get_AxisBetweenCategories](./get_axisbetweencategories/). |
| [set_BaseTimeUnit](./set_basetimeunit/)(Aspose::Words::Drawing::Charts::AxisTimeUnit) | Setzer für [Aspose::Words::Drawing::Charts::ChartAxis::get_BaseTimeUnit](./get_basetimeunit/). |
| [set_CategoryType](./set_categorytype/)(Aspose::Words::Drawing::Charts::AxisCategoryType) | Setzer für [Aspose::Words::Drawing::Charts::ChartAxis::get_CategoryType](./get_categorytype/). |
| [set_Crosses](./set_crosses/)(Aspose::Words::Drawing::Charts::AxisCrosses) | Setzer für [Aspose::Words::Drawing::Charts::ChartAxis::get_Crosses](./get_crosses/). |
| [set_CrossesAt](./set_crossesat/)(double) | Setzer für [Aspose::Words::Drawing::Charts::ChartAxis::get_CrossesAt](./get_crossesat/). |
| [set_HasMajorGridlines](./set_hasmajorgridlines/)(bool) | Setzer für [Aspose::Words::Drawing::Charts::ChartAxis::get_HasMajorGridlines](./get_hasmajorgridlines/). |
| [set_HasMinorGridlines](./set_hasminorgridlines/)(bool) | Setzer für [Aspose::Words::Drawing::Charts::ChartAxis::get_HasMinorGridlines](./get_hasminorgridlines/). |
| [set_Hidden](./set_hidden/)(bool) | Setzer für [Aspose::Words::Drawing::Charts::ChartAxis::get_Hidden](./get_hidden/). |
| [set_MajorTickMark](./set_majortickmark/)(Aspose::Words::Drawing::Charts::AxisTickMark) | Setzer für [Aspose::Words::Drawing::Charts::ChartAxis::get_MajorTickMark](./get_majortickmark/). |
| [set_MajorUnit](./set_majorunit/)(double) | Setzer für [Aspose::Words::Drawing::Charts::ChartAxis::get_MajorUnit](./get_majorunit/). |
| [set_MajorUnitIsAuto](./set_majorunitisauto/)(bool) | Setzer für [Aspose::Words::Drawing::Charts::ChartAxis::get_MajorUnitIsAuto](./get_majorunitisauto/). |
| [set_MajorUnitScale](./set_majorunitscale/)(Aspose::Words::Drawing::Charts::AxisTimeUnit) | Setzer für [Aspose::Words::Drawing::Charts::ChartAxis::get_MajorUnitScale](./get_majorunitscale/). |
| [set_MinorTickMark](./set_minortickmark/)(Aspose::Words::Drawing::Charts::AxisTickMark) | Setzer für [Aspose::Words::Drawing::Charts::ChartAxis::get_MinorTickMark](./get_minortickmark/). |
| [set_MinorUnit](./set_minorunit/)(double) | Setzer für [Aspose::Words::Drawing::Charts::ChartAxis::get_MinorUnit](./get_minorunit/). |
| [set_MinorUnitIsAuto](./set_minorunitisauto/)(bool) | Setzer für [Aspose::Words::Drawing::Charts::ChartAxis::get_MinorUnitIsAuto](./get_minorunitisauto/). |
| [set_MinorUnitScale](./set_minorunitscale/)(Aspose::Words::Drawing::Charts::AxisTimeUnit) | Setzer für [Aspose::Words::Drawing::Charts::ChartAxis::get_MinorUnitScale](./get_minorunitscale/). |
| [set_ReverseOrder](./set_reverseorder/)(bool) | Setzer für [Aspose::Words::Drawing::Charts::ChartAxis::get_ReverseOrder](./get_reverseorder/). |
| [set_TickMarkSpacing](./set_tickmarkspacing/)(int32_t) | Setzer für [Aspose::Words::Drawing::Charts::ChartAxis::get_TickMarkSpacing](./get_tickmarkspacing/). |
| static [Type](./type/)() |  |

## Beispiele



Zeigt, wie man ein Diagramm einfügt und das Aussehen seiner Achsen ändert.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 500, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

// Löschen Sie die Demo-Datenreihe des Diagramms, um mit einem leeren Diagramm zu beginnen.
chart->get_Series()->Clear();

// Fügen Sie eine Diagrammreihe mit Kategorien für die X-Achse und jeweiligen numerischen Werten für die Y-Achse ein.
chart->get_Series()->Add(u"Aspose Test Series", System::MakeArray<System::String>({u"Word", u"PDF", u"Excel", u"GoogleDocs", u"Note"}), System::MakeArray<double>({640, 320, 280, 120, 150}));

// Diagrammachsen haben verschiedene Optionen, die ihr Aussehen verändern können,
// wie z. B. ihre Richtung, Haupt‑/Nebeneinheiten‑Markierungen und Teilstriche.
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

// Säulendiagramme haben keine Z-Achse.
ASSERT_TRUE(System::TestTools::IsNull(chart->get_AxisZ()));

doc->Save(get_ArtifactsDir() + u"Charts.AxisProperties.docx");
```

## Siehe auch

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
