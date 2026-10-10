---
title: "Aspose::Words::TextDmlEffect 枚举"
linktitle: "TextDmlEffect"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::TextDmlEffect 枚举。用于 C++ 中文本运行的 Dml 文本效果。"
type: docs
weight: 122000
url: /zh/cpp/aspose.words/textdmleffect/
---
## TextDmlEffect enum


文本运行的 Dml 文本效果。

```cpp
enum class TextDmlEffect
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| Glow | 0 | Glow 效果，即在对象边缘之外添加颜色模糊轮廓。 |
| Fill | 1 | Fill 覆盖效果。 |
| Shadow | 2 | Shadow 效果。 |
| Outline | 3 | Outline 效果。 |
| Effect3D | 4 | 3D 效果。 |
| 反射 | 5 | 反射效果。 |


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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
