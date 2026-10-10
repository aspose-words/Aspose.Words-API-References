---
title: "Aspose::Words::Settings::ViewOptions Klasse"
linktitle: "ViewOptions"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Settings::ViewOptions Klasse. Bietet verschiedene Optionen, die steuern, wie ein Dokument in Microsoft Word angezeigt wird. Weitere Informationen finden Sie im Dokumentationsartikel in C++."
type: docs
weight: 9000
url: /de/cpp/aspose.words.settings/viewoptions/
---
## ViewOptions class


Bietet verschiedene Optionen, die steuern, wie ein Dokument in Microsoft Word angezeigt wird. Weitere Informationen finden Sie im Dokumentationsartikel [Arbeiten mit Optionen und Erscheinungsbild von Word‑Dokumenten](https://docs.aspose.com/words/cpp/work-with-word-document-options-and-appearance/).

```cpp
class ViewOptions : public System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get_DisplayBackgroundShape](./get_displaybackgroundshape/)() const | Steuert die Anzeige der Hintergrundform in der Drucklayout-Ansicht. |
| [get_DoNotDisplayPageBoundaries](./get_donotdisplaypageboundaries/)() const | Schaltet die Anzeige des Abstands zwischen dem oberen Rand des Textes und dem oberen Rand der Seite aus. |
| [get_FormsDesign](./get_formsdesign/)() const | Gibt an, ob das Dokument sich im Formular-Entwurfsmodus befindet. |
| [get_ViewType](./get_viewtype/)() const | Steuert den Ansichtsmodus in Microsoft Word. |
| [get_ZoomPercent](./get_zoompercent/)() const | Liest oder legt den Prozentsatz fest, mit dem Sie Ihr Dokument anzeigen möchten. |
| [get_ZoomType](./get_zoomtype/)() const | Liest oder legt einen Zoomwert fest, basierend auf der Größe des Fensters. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_DisplayBackgroundShape](./set_displaybackgroundshape/)(bool) | Setter für [Aspose::Words::Settings::ViewOptions::get_DisplayBackgroundShape](./get_displaybackgroundshape/). |
| [set_DoNotDisplayPageBoundaries](./set_donotdisplaypageboundaries/)(bool) | Setter für [Aspose::Words::Settings::ViewOptions::get_DoNotDisplayPageBoundaries](./get_donotdisplaypageboundaries/). |
| [set_FormsDesign](./set_formsdesign/)(bool) | Setter für [Aspose::Words::Settings::ViewOptions::get_FormsDesign](./get_formsdesign/). |
| [set_ViewType](./set_viewtype/)(Aspose::Words::Settings::ViewType) | Setter für [Aspose::Words::Settings::ViewOptions::get_ViewType](./get_viewtype/). |
| [set_ZoomPercent](./set_zoompercent/)(int32_t) | Setter für [Aspose::Words::Settings::ViewOptions::get_ZoomPercent](./get_zoompercent/). |
| [set_ZoomType](./set_zoomtype/)(Aspose::Words::Settings::ZoomType) | Setter für [Aspose::Words::Settings::ViewOptions::get_ZoomType](./get_zoomtype/). |
| static [Type](./type/)() |  |

## Beispiele



Zeigt, wie ein benutzerdefinierter Zoomfaktor festgelegt wird, den ältere Versionen von Microsoft Word beim Laden eines Dokuments anwenden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

doc->get_ViewOptions()->set_ViewType(Aspose::Words::Settings::ViewType::PageLayout);
doc->get_ViewOptions()->set_ZoomPercent(50);

ASSERT_EQ(Aspose::Words::Settings::ZoomType::Custom, doc->get_ViewOptions()->get_ZoomType());
ASSERT_EQ(Aspose::Words::Settings::ZoomType::None, doc->get_ViewOptions()->get_ZoomType());

doc->Save(get_ArtifactsDir() + u"ViewOptions.SetZoomPercentage.doc");
```


Zeigt, wie ein benutzerdefinierter Zoomtyp festgelegt wird, den ältere Versionen von Microsoft Word beim Laden eines Dokuments anwenden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

// Setzen Sie die Eigenschaft "ZoomType" auf "ZoomType.PageWidth", um Microsoft Word zu erhalten.
// um das Dokument automatisch zu zoomen, sodass es die Seitenbreite ausfüllt.
// Setzen Sie die Eigenschaft "ZoomType" auf "ZoomType.FullPage", um Microsoft Word zu erhalten.
// um das Dokument automatisch zu zoomen, sodass die gesamte erste Seite sichtbar wird.
// Setzen Sie die Eigenschaft "ZoomType" auf "ZoomType.TextFit", um Microsoft Word zu erhalten.
// um das Dokument automatisch zu zoomen, sodass die inneren Textränder der ersten Seite passen.
doc->get_ViewOptions()->set_ZoomType(zoomType);

doc->Save(get_ArtifactsDir() + u"ViewOptions.SetZoomType.doc");
```

## Siehe auch

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
