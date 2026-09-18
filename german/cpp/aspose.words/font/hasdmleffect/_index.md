---
title: "Aspose::Words::Font::HasDmlEffect Methode"
linktitle: "HasDmlEffect"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Font::HasDmlEffect Methode. Prüft, ob ein bestimmter DrawingML-Text-Effekt in C++ angewendet wird."
type: docs
weight: 58000
url: /de/cpp/aspose.words/font/hasdmleffect/
---
## Font::HasDmlEffect method


Prüft, ob ein bestimmter DrawingML‑Texteffekt angewendet wird.

```cpp
bool Aspose::Words::Font::HasDmlEffect(Aspose::Words::TextDmlEffect dmlEffectType)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| dmlEffectType | Aspose::Words::TextDmlEffect | DrawingML Texteffekttyp. |

### ReturnValue

**true** if particular DrawingML text effect is applied.

## Beispiele



Zeigt, wie überprüft werden kann, ob ein Lauf einen DrawingML-Texteffekt anzeigt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"DrawingML text effects.docx");

System::SharedPtr<Aspose::Words::RunCollection> runs = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs();

ASSERT_TRUE(runs->idx_get(0)->get_Font()->HasDmlEffect(Aspose::Words::TextDmlEffect::Shadow));
ASSERT_TRUE(runs->idx_get(1)->get_Font()->HasDmlEffect(Aspose::Words::TextDmlEffect::Shadow));
ASSERT_TRUE(runs->idx_get(2)->get_Font()->HasDmlEffect(Aspose::Words::TextDmlEffect::Reflection));
ASSERT_TRUE(runs->idx_get(3)->get_Font()->HasDmlEffect(Aspose::Words::TextDmlEffect::Effect3D));
ASSERT_TRUE(runs->idx_get(4)->get_Font()->HasDmlEffect(Aspose::Words::TextDmlEffect::Fill));
```

## Siehe auch

* Enum [TextDmlEffect](../../textdmleffect/)
* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
