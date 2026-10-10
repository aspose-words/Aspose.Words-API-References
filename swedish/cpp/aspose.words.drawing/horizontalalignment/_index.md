---
title: "Aspose::Words::Drawing::HorizontalAlignment enum"
linktitle: "HorizontalAlignment"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::HorizontalAlignment enum. Anger horisontell justering av en flytande form, textruta eller flytande tabell i C++."
type: docs
weight: 26000
url: /sv/cpp/aspose.words.drawing/horizontalalignment/
---
## HorizontalAlignment enum


Anger horisontell justering av en flytande form, textram eller flytande tabell.

```cpp
enum class HorizontalAlignment
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| None | 0 | Objektet placeras explicit, vanligtvis med dess **Left**‑egenskap. |
| Default | n/a | Samma som [None](./). |
| Vänster | 1 | Anger att objektet ska vara vänsterjusterat mot den horisontella justeringsbasen. |
| Centrerad | 2 | Anger att objektet ska centreras i förhållande till den horisontella justeringsbasen. |
| Höger | 3 | Anger att objektet ska vara högerjusterat mot den horisontella justeringsbasen. |
| Inuti | 4 | Anger att objektet ska vara inuti den horisontella justeringsbasen. |
| Utom | 5 | Anger att objektet ska placeras utanför den horisontella justeringsbasen. |


## Exempel



Visar hur man infogar en flytande bild i sidans centrum.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Infoga en flytande bild som visas bakom den överlappande texten och justera den till sidans centrum.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);
shape->set_BehindText(true);
shape->set_RelativeHorizontalPosition(Aspose::Words::Drawing::RelativeHorizontalPosition::Page);
shape->set_RelativeVerticalPosition(Aspose::Words::Drawing::RelativeVerticalPosition::Page);
shape->set_HorizontalAlignment(Aspose::Words::Drawing::HorizontalAlignment::Center);
shape->set_VerticalAlignment(Aspose::Words::Drawing::VerticalAlignment::Center);

doc->Save(get_ArtifactsDir() + u"Image.CreateFloatingPageCenter.docx");
```

## Se även

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
