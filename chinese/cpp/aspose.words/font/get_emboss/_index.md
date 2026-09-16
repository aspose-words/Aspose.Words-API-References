---
title: "Aspose::Words::Font::get_Emboss 方法"
linktitle: "get_Emboss"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Font::get_Emboss 方法。若字体在 C++ 中被设置为浮雕效果则为 true。"
type: docs
weight: 12000
url: /zh/cpp/aspose.words/font/get_emboss/
---
## Font::get_Emboss method


如果字体格式为浮雕效果，则为 True。

```cpp
bool Aspose::Words::Font::get_Emboss()
```


## 示例



展示如何对文本应用雕刻/浮雕效果。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Size(36);
builder->get_Font()->set_Color(System::Drawing::Color::get_LightBlue());

// 下面展示了两种使用阴影为文本应用类似 3D 效果的方法。
// 1 -  雕刻文本，使字母看起来像凹入页面：
builder->get_Font()->set_Engrave(true);

builder->Writeln(u"This text is engraved.");

// 2 -  浮雕文本，使字母看起来像凸出页面：
builder->get_Font()->set_Engrave(false);
builder->get_Font()->set_Emboss(true);

builder->Writeln(u"This text is embossed.");

doc->Save(get_ArtifactsDir() + u"Font.EngraveEmboss.docx");
```

## 另见

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
