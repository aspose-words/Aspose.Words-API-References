---
title: "Aspose::Words::Font::get_TextEffect 方法"
linktitle: "get_TextEffect"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Font::get_TextEffect 方法。获取或设置 C++ 中的字体动画效果。"
type: docs
weight: 47000
url: /zh/cpp/aspose.words/font/get_texteffect/
---
## Font::get_TextEffect method


获取或设置字体动画效果。

```cpp
Aspose::Words::TextEffect Aspose::Words::Font::get_TextEffect()
```


## 示例



展示如何对文本运行应用视觉效果。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Size(36);
builder->get_Font()->set_TextEffect(Aspose::Words::TextEffect::SparkleText);

builder->Writeln(u"Text with a sparkle effect.");

// 较旧版本的 Microsoft Word 仅支持字体动画效果。
doc->Save(get_ArtifactsDir() + u"Font.SparklingText.doc");
```

## 另见

* Enum [TextEffect](../../texteffect/)
* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
