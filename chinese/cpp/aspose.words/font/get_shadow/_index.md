---
title: "Aspose::Words::Font::get_Shadow 方法"
linktitle: "get_Shadow"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Font::get_Shadow 方法。如果字体在 C++ 中被设置为阴影格式，则为 true。"
type: docs
weight: 35000
url: /zh/cpp/aspose.words/font/get_shadow/
---
## Font::get_Shadow method


如果字体被格式化为带阴影，则为 True。

```cpp
bool Aspose::Words::Font::get_Shadow()
```


## 示例



展示如何创建带阴影格式的文本运行。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 设置 Shadow 标志以应用偏移阴影效果，
// 使字母看起来像漂浮在页面上方。
builder->get_Font()->set_Shadow(true);
builder->get_Font()->set_Size(36);

builder->Writeln(u"This text has a shadow.");

doc->Save(get_ArtifactsDir() + u"Font.Shadow.docx");
```

## 另见

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
