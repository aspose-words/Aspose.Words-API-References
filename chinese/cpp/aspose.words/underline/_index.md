---
title: "Aspose::Words::Underline enum"
linktitle: "下划线"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Underline 枚举。指示在 C++ 中应用于字体的下划线类型。"
type: docs
weight: 126000
url: /zh/cpp/aspose.words/underline/
---
## Underline enum


指示应用于字体的下划线类型。

```cpp
enum class Underline
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| None | 0 |  |
| 单线 | 1 |  |
| 单词 | 2 |  |
| 双线 | 3 |  |
| 点线 | 4 |  |
| 粗线 | 6 |  |
| 短划线 | 7 |  |
| 长划线 | 39 |  |
| 点划线 | 9 |  |
| DotDotDash | 10 |  |
| Wavy | 11 |  |
| DottedHeavy | 20 |  |
| DashHeavy | 23 |  |
| DashLongHeavy | 55 |  |
| DotDashHeavy | 25 |  |
| DotDotDashHeavy | 26 |  |
| WavyHeavy | 27 |  |
| WavyDouble | 43 |  |


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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
