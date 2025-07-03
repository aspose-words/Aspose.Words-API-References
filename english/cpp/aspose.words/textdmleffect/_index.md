---
title: Aspose::Words::TextDmlEffect enum
linktitle: TextDmlEffect
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::TextDmlEffect enum. Dml text effect for text runs in C++.'
type: docs
weight: 122000
url: /cpp/aspose.words/textdmleffect/
---
## TextDmlEffect enum


Dml text effect for text runs.

```cpp
enum class TextDmlEffect
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Glow | 0 | Glow effect, in which a color blurred outline is added outside the edges of the object. |
| Fill | 1 | Fill overlay effect. |
| Shadow | 2 | Shadow effect. |
| Outline | 3 | Outline effect. |
| Effect3D | 4 | 3D effect. |
| Reflection | 5 | Reflection effect. |


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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
