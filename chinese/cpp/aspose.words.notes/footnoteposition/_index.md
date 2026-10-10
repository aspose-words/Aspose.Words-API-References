---
title: "Aspose::Words::Notes::FootnotePosition enum"
linktitle: "FootnotePosition"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Notes::FootnotePosition 枚举。定义了 C++ 中的脚注位置。"
type: docs
weight: 6000
url: /zh/cpp/aspose.words.notes/footnoteposition/
---
## FootnotePosition enum


定义脚注位置。

```cpp
enum class FootnotePosition
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| BottomOfPage | 1 | 脚注会输出在每页的底部。 |
| BeneathText | 2 | 脚注会输出在每页文本的下方。 |


## 示例



展示如何选择文档收集并显示脚注的不同位置。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 脚注是一种将参考或旁注附加到文本的方式
// 且不会干扰正文文本的流畅性。
// 插入脚注会添加一个小的上标参考符号
// 在我们插入脚注的正文文本中。
// 每个脚注还会在页面底部创建一个条目，该条目由一个符号组成
// 该符号与正文中的引用符号相匹配。
// 我们传递给文档生成器的 "InsertFootnote" 方法的参考文本。
builder->Write(u"Hello world!");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote contents.");

// 我们可以使用 "Position" 属性来确定文档将在何处放置所有脚注。
// 如果我们将 "Position" 属性的值设置为 "FootnotePosition.BottomOfPage"，
// 每个脚注都会显示在包含其参考标记的页面底部。这是默认值。
// 如果我们将 "Position" 属性的值设置为 "FootnotePosition.BeneathText"，
// 每个脚注都会显示在包含其参考标记的页面文本的末尾。
doc->get_FootnoteOptions()->set_Position(footnotePosition);

doc->Save(get_ArtifactsDir() + u"InlineStory.PositionFootnote.docx");
```

## 另见

* Namespace [Aspose::Words::Notes](../)
* Library [Aspose.Words for C++](../../)
