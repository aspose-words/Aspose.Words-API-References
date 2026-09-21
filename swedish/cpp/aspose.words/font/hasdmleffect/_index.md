---
title: "Aspose::Words::Font::HasDmlEffect method"
linktitle: "HasDmlEffect"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Font::HasDmlEffect method. Kontrollerar om en viss DrawingML-text effekt är tillämpad i C++."
type: docs
weight: 58000
url: /sv/cpp/aspose.words/font/hasdmleffect/
---
## Font::HasDmlEffect method


Kontrollerar om en viss DrawingML‑texteffekt har tillämpats.

```cpp
bool Aspose::Words::Font::HasDmlEffect(Aspose::Words::TextDmlEffect dmlEffectType)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| dmlEffectType | Aspose::Words::TextDmlEffect | DrawingML-texteffekttyp. |

### ReturnValue

**true** if particular DrawingML text effect is applied.

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

* Enum [TextDmlEffect](../../textdmleffect/)
* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
