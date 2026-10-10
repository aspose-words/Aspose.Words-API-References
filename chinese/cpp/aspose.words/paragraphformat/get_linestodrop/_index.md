---
title: "Aspose::Words::ParagraphFormat::get_LinesToDrop 方法"
linktitle: "get_LinesToDrop"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::ParagraphFormat::get_LinesToDrop 方法。获取或设置用于计算首字母下沉高度的段落文本行数（在 C++ 中）。"
type: docs
weight: 22000
url: /zh/cpp/aspose.words/paragraphformat/get_linestodrop/
---
## ParagraphFormat::get_LinesToDrop method


获取或设置用于计算首字母放大高度的段落文本行数。

```cpp
int32_t Aspose::Words::ParagraphFormat::get_LinesToDrop()
```


## 示例



展示如何设置首字母下沉的大小。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 修改 "LinesToDrop" 属性以将段落指定为首字母下沉，
// 这将把它变成一个装饰下一段落的大写字母。
// 将此属性设置为 4，使首字母下沉的高度为四行文本。
builder->get_ParagraphFormat()->set_LinesToDrop(4);
builder->Writeln(u"H");

// 将 "LinesToDrop" 属性重置为 0，使下一段落恢复为普通段落。
// 此段落中的文本将环绕首字母下沉。
builder->get_ParagraphFormat()->set_LinesToDrop(0);
builder->Writeln(u"ello world!");

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.LinesToDrop.odt");
```

## 另见

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
