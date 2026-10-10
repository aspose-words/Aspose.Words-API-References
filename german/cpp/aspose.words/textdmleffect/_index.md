---
title: "Aspose::Words::TextDmlEffect Enum"
linktitle: "TextDmlEffect"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::TextDmlEffect Enum. DML-Texteffekt für Textläufe in C++."
type: docs
weight: 122000
url: /de/cpp/aspose.words/textdmleffect/
---
## TextDmlEffect enum


Dml-Text-Effekt für Textläufe.

```cpp
enum class TextDmlEffect
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Leuchten | 0 | Leuchte-Effekt, bei dem ein farblich unscharfer Umriss außerhalb der Objektkanten hinzugefügt wird. |
| Füllung | 1 | Füll-Overlay-Effekt. |
| Schatten | 2 | Schatten-Effekt. |
| Umriss | 3 | Umriss-Effekt. |
| Effect3D | 4 | 3D-Effekt. |
| Reflexion | 5 | Reflexions-Effekt. |


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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
