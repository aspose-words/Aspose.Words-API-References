---
title: "Aspose::Words::Settings::ZoomType enum"
linktitle: "ZoomType"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Settings::ZoomType enum. Möjliga värden för hur stor eller liten dokumentet visas på skärmen i Microsoft Word i C++."
type: docs
weight: 22000
url: /sv/cpp/aspose.words.settings/zoomtype/
---
## ZoomType enum


Möjliga värden för hur stort eller litet dokumentet visas på skärmen i Microsoft Word.

```cpp
enum class ZoomType
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| Anpassad | 0 | Zoomprocenten sätts explicit. Den beräknas inte om automatiskt när kontrollens storlek ändras. |
| None | n/a | Indikerar att den explicita zoomprocenten ska användas. Samma som [Custom](./). |
| FullPage | 1 | Zoomprocenten beräknas automatiskt om för att passa en hel sida. |
| PageWidth | 2 | Zoomprocenten beräknas automatiskt om för att passa sidbredden. |
| TextFit | 3 | Zoomprocenten beräknas automatiskt om för att passa texten. |


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
