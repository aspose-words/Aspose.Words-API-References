---
title: "Aspose::Words::Font::HasDmlEffect 方法"
linktitle: "HasDmlEffect"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Font::HasDmlEffect 方法。检查是否在 C++ 中应用了特定的 DrawingML 文本效果。"
type: docs
weight: 58000
url: /zh/cpp/aspose.words/font/hasdmleffect/
---
## Font::HasDmlEffect method


检查是否已应用特定的 DrawingML 文本效果。

```cpp
bool Aspose::Words::Font::HasDmlEffect(Aspose::Words::TextDmlEffect dmlEffectType)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| dmlEffectType | Aspose::Words::TextDmlEffect | DrawingML 文本效果类型。 |

### ReturnValue

**true** if particular DrawingML text effect is applied.

## 示例



展示如何检查运行是否显示 DrawingML 文本效果。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"DrawingML text effects.docx");

System::SharedPtr<Aspose::Words::RunCollection> runs = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs();

ASSERT_TRUE(runs->idx_get(0)->get_Font()->HasDmlEffect(Aspose::Words::TextDmlEffect::Shadow));
ASSERT_TRUE(runs->idx_get(1)->get_Font()->HasDmlEffect(Aspose::Words::TextDmlEffect::Shadow));
ASSERT_TRUE(runs->idx_get(2)->get_Font()->HasDmlEffect(Aspose::Words::TextDmlEffect::Reflection));
ASSERT_TRUE(runs->idx_get(3)->get_Font()->HasDmlEffect(Aspose::Words::TextDmlEffect::Effect3D));
ASSERT_TRUE(runs->idx_get(4)->get_Font()->HasDmlEffect(Aspose::Words::TextDmlEffect::Fill));
```

## 另见

* Enum [TextDmlEffect](../../textdmleffect/)
* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
