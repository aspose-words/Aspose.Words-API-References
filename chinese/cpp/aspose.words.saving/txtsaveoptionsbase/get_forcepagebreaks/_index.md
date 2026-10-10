---
title: "Aspose::Words::Saving::TxtSaveOptionsBase::get_ForcePageBreaks 方法"
linktitle: "get_ForcePageBreaks"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::TxtSaveOptionsBase::get_ForcePageBreaks 方法。允许指定在导出时是否应保留分页符。默认值在 C++ 中为 false。"
type: docs
weight: 5000
url: /zh/cpp/aspose.words.saving/txtsaveoptionsbase/get_forcepagebreaks/
---
## TxtSaveOptionsBase::get_ForcePageBreaks method


允许指定在导出时是否应保留分页符。默认值为 **false**。

```cpp
bool Aspose::Words::Saving::TxtSaveOptionsBase::get_ForcePageBreaks() const
```


## 示例



展示如何在将文档导出为纯文本时指定是否保留分页符。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Page 1");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 2");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 3");

// 创建一个 "TxtSaveOptions" 对象，我们可以将其传递给文档的 "Save"
// 方法用于修改我们将文档保存为纯文本的方式。
auto saveOptions = System::MakeObject<Aspose::Words::Saving::TxtSaveOptions>();

// Aspose.Words 的 "Document" 对象具有分页符，就像 Microsoft Word 文档一样。
// 保存格式，例如 ".txt"，是没有分页符的连续文本。
// 将 "ForcePageBreaks" 属性设置为 "true"，以使用 '\f' 字符的形式保留所有分页符。
// 将 "ForcePageBreaks" 属性设置为 "false"，以丢弃所有分页符。
saveOptions->set_ForcePageBreaks(forcePageBreaks);

doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.PageBreaks.txt", saveOptions);

// 如果我们加载带有分页符的纯文本文档，
// "Document" 对象将使用它们将正文拆分为页面。
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"TxtSaveOptions.PageBreaks.txt");

ASSERT_EQ(forcePageBreaks ? 3 : 1, doc->get_PageCount());
```

## 另见

* Class [TxtSaveOptionsBase](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
