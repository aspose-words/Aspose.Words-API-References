---
title: "Aspose::Words::Document::get_GrammarChecked 方法"
linktitle: "get_GrammarChecked"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Document::get_GrammarChecked 方法。返回 true，如果文档已在 C++ 中进行语法检查。"
type: docs
weight: 29000
url: /zh/cpp/aspose.words/document/get_grammarchecked/
---
## Document::get_GrammarChecked method


如果已对文档进行语法检查，则返回 **true**。

```cpp
bool Aspose::Words::Document::get_GrammarChecked()
```


## 示例



展示如何设置拼写或语法验证。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// 包含拼写错误的字符串。
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->Add(System::MakeObject<Aspose::Words::Run>(doc, u"The speeling in this documentz is all broked."));

// 如果我们将属性设置为 false，则启动拼写/语法检查。
// 我们可以在 Microsoft Word 中通过审阅 -> 拼写和语法 查看所有错误。
// 请注意，Microsoft Word 不会自动启动 DOC 和 RTF 文档格式的语法/拼写检查。
doc->set_SpellingChecked(checkSpellingGrammar);
doc->set_GrammarChecked(checkSpellingGrammar);

doc->Save(get_ArtifactsDir() + u"Document.SpellingOrGrammar.docx");
```

## 另见

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
