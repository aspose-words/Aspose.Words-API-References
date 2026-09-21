---
title: "Aspose::Words::TextDmlEffect enum"
linktitle: "TextDmlEffect"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::TextDmlEffect enum. Dml‑texteffekt för textkörningar i C++."
type: docs
weight: 122000
url: /sv/cpp/aspose.words/textdmleffect/
---
## TextDmlEffect enum


Dml‑texteffekt för textkörningar.

```cpp
enum class TextDmlEffect
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| Glow | 0 | Glöd‑effekt, där en färgad suddig kontur läggs till utanför objektets kanter. |
| Fill | 1 | Fyll‑överlappningseffekt. |
| Shadow | 2 | Skuggeffekt. |
| Outline | 3 | Kontureffekt. |
| Effect3D | 4 | 3D‑effekt. |
| Reflection | 5 | Reflektionseffekt. |


## Exempel



Visar hur man kontrollerar om ett körningsobjekt visar en DrawingML‑texteffekt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"DrawingML text effects.docx");

System::SharedPtr<Aspose::Words::RunCollection> runs = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs();

ASSERT_TRUE(runs->idx_get(0)->get_Font()->HasDmlEffect(Aspose::Words::TextDmlEffect::Shadow));
ASSERT_TRUE(runs->idx_get(1)->get_Font()->HasDmlEffect(Aspose::Words::TextDmlEffect::Shadow));
ASSERT_TRUE(runs->idx_get(2)->get_Font()->HasDmlEffect(Aspose::Words::TextDmlEffect::Reflection));
ASSERT_TRUE(runs->idx_get(3)->get_Font()->HasDmlEffect(Aspose::Words::TextDmlEffect::Effect3D));
ASSERT_TRUE(runs->idx_get(4)->get_Font()->HasDmlEffect(Aspose::Words::TextDmlEffect::Fill));
```

## Se även

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
