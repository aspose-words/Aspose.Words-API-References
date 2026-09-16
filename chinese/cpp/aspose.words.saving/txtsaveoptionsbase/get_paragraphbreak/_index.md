---
title: "Aspose::Words::Saving::TxtSaveOptionsBase::get_ParagraphBreak 方法"
linktitle: "get_ParagraphBreak"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::TxtSaveOptionsBase::get_ParagraphBreak 方法。指定在 C++ 中以文本格式导出时用作段落换行的字符串。"
type: docs
weight: 6000
url: /zh/cpp/aspose.words.saving/txtsaveoptionsbase/get_paragraphbreak/
---
## TxtSaveOptionsBase::get_ParagraphBreak method


指定在文本格式导出时用作段落换行的字符串。

```cpp
System::String Aspose::Words::Saving::TxtSaveOptionsBase::get_ParagraphBreak() const
```

## 备注


默认值是 [CrLf](../../../aspose.words/controlchar/crlf/)。

## 示例



展示如何使用自定义段落换行保存 .txt 文档。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Paragraph 1.");
builder->Writeln(u"Paragraph 2.");
builder->Write(u"Paragraph 3.");

// 创建一个 "TxtSaveOptions" 对象，可将其传递给文档的 "Save" 方法
// 以修改我们保存文档为纯文本的方式。
auto txtSaveOptions = System::MakeObject<Aspose::Words::Saving::TxtSaveOptions>();

ASSERT_EQ(Aspose::Words::SaveFormat::Text, txtSaveOptions->get_SaveFormat());

// 将 "ParagraphBreak" 设置为我们希望放在每个段落末尾的自定义值。
txtSaveOptions->set_ParagraphBreak(u" End of paragraph.\n\n\t");

doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.ParagraphBreak.txt", txtSaveOptions);

System::String docText = System::IO::File::ReadAllText(get_ArtifactsDir() + u"TxtSaveOptions.ParagraphBreak.txt");

ASSERT_EQ(System::String(u"Paragraph 1. End of paragraph.\n\n\t") + u"Paragraph 2. End of paragraph.\n\n\t" + u"Paragraph 3. End of paragraph.\n\n\t", docText);
```

## 另见

* Class [TxtSaveOptionsBase](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
