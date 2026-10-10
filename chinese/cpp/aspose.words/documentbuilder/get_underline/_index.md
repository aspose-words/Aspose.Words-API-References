---
title: "Aspose::Words::DocumentBuilder::get_Underline 方法"
linktitle: "get_Underline"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::DocumentBuilder::get_Underline 方法。获取/设置当前字体的下划线类型（C++）。"
type: docs
weight: 26000
url: /zh/cpp/aspose.words/documentbuilder/get_underline/
---
## DocumentBuilder::get_Underline method


获取/设置当前字体的下划线类型。

```cpp
Aspose::Words::Underline Aspose::Words::DocumentBuilder::get_Underline()
```


## 示例



展示如何格式化文档构建器插入的文本。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->set_Underline(Aspose::Words::Underline::Dash);
builder->get_Font()->set_Color(System::Drawing::Color::get_Blue());
builder->get_Font()->set_Size(32);

// 构建器会对其当前段落以及随后添加的任何新文本应用格式。
builder->Writeln(u"Large, blue, and underlined text.");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertUnderline.docx");
```

## 另见

* Enum [Underline](../../underline/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
