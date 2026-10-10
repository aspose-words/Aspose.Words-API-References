---
title: "Aspose::Words::ParagraphFormat::get_LeftIndent method"
linktitle: "get_LeftIndent"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::ParagraphFormat::get_LeftIndent method. 获取或设置表示段落左缩进的值（单位为点）（C++）。"
type: docs
weight: 19000
url: /zh/cpp/aspose.words/paragraphformat/get_leftindent/
---
## ParagraphFormat::get_LeftIndent method


获取或设置表示段落左缩进的值（以点为单位）。

```cpp
double Aspose::Words::ParagraphFormat::get_LeftIndent()
```


## 示例



展示如何配置段落格式以创建偏离中心的文本。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 将文档生成器写入的所有文本居中，并设置缩进。
// 下面的缩进配置将创建一段在页面上不对称排列的文本。
// 我们对齐文本的 “center” 将是文本主体的中间，而不是页面的中间。
System::SharedPtr<Aspose::Words::ParagraphFormat> paragraphFormat = builder->get_ParagraphFormat();
paragraphFormat->set_Alignment(Aspose::Words::ParagraphAlignment::Center);
paragraphFormat->set_LeftIndent(100);
paragraphFormat->set_RightIndent(50);
paragraphFormat->set_SpaceAfter(25);

builder->Writeln(u"This paragraph demonstrates how left and right indentation affects word wrapping.");
builder->Writeln(u"The space between the above paragraph and this one depends on the DocumentBuilder's paragraph format.");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.SetParagraphFormatting.docx");
```

## 另见

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
