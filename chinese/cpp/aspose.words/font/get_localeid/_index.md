---
title: "Aspose::Words::Font::get_LocaleId 方法"
linktitle: "get_LocaleId"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Font::get_LocaleId 方法。获取或设置 C++ 中格式化字符的区域标识符（语言）。"
type: docs
weight: 22000
url: /zh/cpp/aspose.words/font/get_localeid/
---
## Font::get_LocaleId method


获取或设置已格式化字符的区域标识符（语言）。

```cpp
int32_t Aspose::Words::Font::get_LocaleId()
```


## 示例



展示如何使用文档生成器设置我们即将添加的文本的区域设置。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 如果我们将字体的区域设置为英文并插入一些俄文文本，
// 英文区域的拼写检查器将无法识别该文本，并将其标记为拼写错误。
builder->get_Font()->set_LocaleId(System::MakeObject<System::Globalization::CultureInfo>(u"en-US", false)->get_LCID());
builder->Writeln(u"Привет!");

// 为即将添加的文本设置匹配的区域，以使用相应的拼写检查器。
builder->get_Font()->set_LocaleId(System::MakeObject<System::Globalization::CultureInfo>(u"ru-RU", false)->get_LCID());
builder->Writeln(u"Привет!");

doc->Save(get_ArtifactsDir() + u"Font.LocaleId.docx");
```

## 另见

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
