---
title: "Aspose::Words::Font::ClearFormatting 方法"
linktitle: "ClearFormatting"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Font::ClearFormatting 方法。将字体格式重置为 C++ 中的默认设置。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words/font/clearformatting/
---
## Font::ClearFormatting method


重置为默认字体格式。

```cpp
void Aspose::Words::Font::ClearFormatting()
```

## 备注


删除从获取 [Font](../) 的对象上显式指定的所有字体格式，以便字体格式将从相应的父级继承。

## 示例



展示如何插入超链接字段。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"For more information, please visit the ");

// 插入超链接并使用自定义格式进行强调。
// 该超链接将是可点击的文本，能够将我们带到 URL 中指定的位置。
builder->get_Font()->set_Color(System::Drawing::Color::get_Blue());
builder->get_Font()->set_Underline(Aspose::Words::Underline::Single);
builder->InsertHyperlink(u"Google website", u"https://www.google.com", false);
builder->get_Font()->ClearFormatting();
builder->Writeln(u".");

// 在 Microsoft Word 中按 Ctrl 并左键单击文本中的链接，将通过新建的网页浏览器窗口打开该 URL。
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertHyperlink.docx");
```

## 另见

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
