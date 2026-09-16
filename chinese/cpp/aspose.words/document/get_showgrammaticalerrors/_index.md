---
title: "Aspose::Words::Document::get_ShowGrammaticalErrors 方法"
linktitle: "get_ShowGrammaticalErrors"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Document::get_ShowGrammaticalErrors 方法。指定是否在此文档中显示语法错误（C++）。"
type: docs
weight: 50000
url: /zh/cpp/aspose.words/document/get_showgrammaticalerrors/
---
## Document::get_ShowGrammaticalErrors method


指定是否在此文档中显示语法错误。

```cpp
bool Aspose::Words::Document::get_ShowGrammaticalErrors()
```


## 示例



展示如何在文档中显示/隐藏错误。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 插入两句包含错误的句子，这些错误将被检测到
// 由 Microsoft Word 中的拼写和语法检查器检测。
builder->Writeln(u"There is a speling error in this sentence.");
builder->Writeln(u"Their is a grammatical error in this sentence.");

// 如果启用这些选项，拼写错误将被下划线标记
// 在输出文档中显示为锯齿形红线，双蓝线将突出显示语法错误。
doc->set_ShowGrammaticalErrors(showErrors);
doc->set_ShowSpellingErrors(showErrors);

doc->Save(get_ArtifactsDir() + u"Document.SpellingAndGrammarErrors.docx");
```

## 另见

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
