---
title: "Aspose::Words::Drawing::VerticalAlignment enum"
linktitle: "VerticalAlignment"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::VerticalAlignment enum. Anger vertikal justering av en flytande form, textruta eller en flytande tabell i C++."
type: docs
weight: 43000
url: /sv/cpp/aspose.words.drawing/verticalalignment/
---
## VerticalAlignment enum


Anger vertikal justering av en flytande form, textruta eller ett flytande bord.

```cpp
enum class VerticalAlignment
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| None | 0 | Objektet är explicit placerat, vanligtvis med hjälp av dess **Top**‑egenskap. |
| Top | 1 | Anger att objektet ska vara högst upp på den vertikala justeringsbasen. |
| Centrerad | 2 | Anger att objektet ska vara centrerat i förhållande till den vertikala justeringsbasen. |
| Bottom | 3 | Anger att objektet ska vara längst ner på den vertikala justeringsbasen. |
| Inuti | 4 | Anger att objektet ska vara inuti den horisontella justeringsbasen. |
| Utom | 5 | Anger att objektet ska vara utanför den vertikala justeringsbasen. |
| Inbäddad | -1 | Ej dokumenterad. Verkar vara ett möjligt värde för flytande stycken och tabeller. |
| Default | n/a | Samma som [None](./). |


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
