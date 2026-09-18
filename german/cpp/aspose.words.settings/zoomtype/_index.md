---
title: "Aspose::Words::Settings::ZoomType enum"
linktitle: "ZoomType"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Settings::ZoomType enum. Mögliche Werte dafür, wie groß oder klein das Dokument in Microsoft Word auf dem Bildschirm angezeigt wird, in C++."
type: docs
weight: 22000
url: /de/cpp/aspose.words.settings/zoomtype/
---
## ZoomType enum


Mögliche Werte dafür, wie groß oder klein das Dokument auf dem Bildschirm in Microsoft Word angezeigt wird.

```cpp
enum class ZoomType
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Benutzerdefiniert | 0 | Der Zoom-Prozentsatz wird explizit festgelegt. Er wird nicht automatisch neu berechnet, wenn sich die Größe der Steuerung ändert. |
| None | n/a | Gibt an, den expliziten Zoom-Prozentsatz zu verwenden. Gleich wie [Custom](./). |
| FullPage | 1 | Der Zoom-Prozentsatz wird automatisch neu berechnet, um eine ganze Seite anzupassen. |
| PageWidth | 2 | Der Zoom-Prozentsatz wird automatisch neu berechnet, um die Seitenbreite anzupassen. |
| TextFit | 3 | Der Zoom-Prozentsatz wird automatisch neu berechnet, um den Text anzupassen. |


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

## Siehe auch

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
