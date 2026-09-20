---
title: "Aspose::Words::TextEffect enum"
linktitle: "TextEffect"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::TextEffect 枚举。C++ 中文本运行的动画效果。"
type: docs
weight: 123000
url: /zh/cpp/aspose.words/texteffect/
---
## TextEffect enum


文本运行的动画效果。

```cpp
enum class TextEffect
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| None | 0 |  |
| LasVegasLights | 1 |  |
| BlinkingBackground | 2 |  |
| SparkleText | 3 |  |
| MarchingBlackAnts | 4 |  |
| MarchingRedAnts | 5 |  |
| Shimmer | 6 |  |


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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
