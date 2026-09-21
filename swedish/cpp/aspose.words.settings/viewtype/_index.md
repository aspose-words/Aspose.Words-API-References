---
title: "Aspose::Words::Settings::ViewType enum"
linktitle: "ViewType"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Settings::ViewType enum. Möjliga värden för visningsläget i Microsoft Word i C++."
type: docs
weight: 21000
url: /sv/cpp/aspose.words.settings/viewtype/
---
## ViewType enum


Möjliga värden för visningsläget i Microsoft Word.

```cpp
enum class ViewType
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| None | 0 | Dokumentet ska renderas i applikationens standardvy. |
| Reading | 0 | Dokumentet ska renderas i applikationens standardvy. |
| PageLayout | 1 | Dokumentet ska öppnas i en vy som visar dokumentet som det kommer att skrivas ut. |
| Outline | 3 | Dokumentet ska renderas i en vy optimerad för att skapa dispositioner eller långa dokument. |
| Normal | 4 | Dokumentet ska renderas i en vy optimerad för att skapa dispositioner eller långa dokument. |
| Web | 5 | Dokumentet ska renderas i en vy som efterliknar hur detta dokument skulle visas på en webbsida. |


## Exempel



Visar hur man ställer in en anpassad zoomfaktor, som äldre versioner av Microsoft Word kommer att tillämpa på ett dokument vid inläsning.
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

## Se även

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
