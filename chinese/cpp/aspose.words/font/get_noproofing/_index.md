---
title: "Aspose::Words::Font::get_NoProofing 方法"
linktitle: "get_NoProofing"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Font::get_NoProofing 方法。当在 C++ 中格式化的字符不进行拼写检查时返回 true。"
type: docs
weight: 30000
url: /zh/cpp/aspose.words/font/get_noproofing/
---
## Font::get_NoProofing method


当已格式化的字符不进行拼写检查时为 True。

```cpp
bool Aspose::Words::Font::get_NoProofing()
```


## 示例



展示如何阻止 Microsoft Word 对文本进行拼写检查。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 通常，Microsoft Word 会使用锯齿形红色下划线来强调拼写错误。
// 我们可以取消设置 "NoProofing" 标志，以创建一段文本，使其
// 绕过拼写检查器，同时完全禁用它。
builder->get_Font()->set_NoProofing(true);

builder->Writeln(u"Proofing has been disabled, so these spelking errrs will not display red lines underneath.");

doc->Save(get_ArtifactsDir() + u"Font.NoProofing.docx");
```

## 另见

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
