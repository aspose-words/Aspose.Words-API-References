---
title: Aspose::Words::Font::HasDmlEffect method
linktitle: HasDmlEffect
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Font::HasDmlEffect method. Checks if particular DrawingML text effect is applied in C++.'
type: docs
weight: 58000
url: /cpp/aspose.words/font/hasdmleffect/
---
## Font::HasDmlEffect method


Checks if particular DrawingML text effect is applied.

```cpp
bool Aspose::Words::Font::HasDmlEffect(Aspose::Words::TextDmlEffect dmlEffectType)
```


| Parameter | Type | Description |
| --- | --- | --- |
| dmlEffectType | Aspose::Words::TextDmlEffect | DrawingML text effect type. |

### ReturnValue

**true** if particular DrawingML text effect is applied.

## Examples



Shows how to check if a run displays a DrawingML text effect. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"DrawingML text effects.docx");

System::SharedPtr<Aspose::Words::RunCollection> runs = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs();

ASSERT_TRUE(runs->idx_get(0)->get_Font()->HasDmlEffect(Aspose::Words::TextDmlEffect::Shadow));
ASSERT_TRUE(runs->idx_get(1)->get_Font()->HasDmlEffect(Aspose::Words::TextDmlEffect::Shadow));
ASSERT_TRUE(runs->idx_get(2)->get_Font()->HasDmlEffect(Aspose::Words::TextDmlEffect::Reflection));
ASSERT_TRUE(runs->idx_get(3)->get_Font()->HasDmlEffect(Aspose::Words::TextDmlEffect::Effect3D));
ASSERT_TRUE(runs->idx_get(4)->get_Font()->HasDmlEffect(Aspose::Words::TextDmlEffect::Fill));
```

## See Also

* Enum [TextDmlEffect](../../textdmleffect/)
* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
