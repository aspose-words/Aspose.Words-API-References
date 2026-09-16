---
title: "Aspose::Words::TabLeader 枚举"
linktitle: "TabLeader"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::TabLeader 枚举。指定在 C++ 中制表符字符下显示的前导线类型。"
type: docs
weight: 121000
url: /zh/cpp/aspose.words/tableader/
---
## TabLeader enum


指定在制表符下显示的前导线的类型。

```cpp
enum class TabLeader
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| None | 0 | 不显示前导线。 |
| 点 | 1 | 前导线由点组成。 |
| 破折号 | 2 | 前导线由破折号组成。 |
| 线 | 3 | 前导线是一条单线。 |
| 粗体 | 4 | 引导线是一条单一的粗线。 |
| 中点 | 5 | 引导线由中点组成。 |


## 示例



展示如何为段落设置自定义制表位。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Paragraph> para = doc->get_FirstSection()->get_Body()->get_FirstParagraph();

// 如果我们在一个段落中，此集合没有制表位，
// 光标在 Microsoft Word 中每次按 Tab 键时会跳跃 36 点。
ASSERT_EQ(0, doc->get_FirstSection()->get_Body()->get_FirstParagraph()->GetEffectiveTabStops()->get_Length());

// 如果我们通过 “View” 选项卡启用标尺，就可以在 Microsoft Word 中添加自定义制表位。
// 此标尺上的每个单位相当于两个默认制表位，即 72 点。
// 我们可以像这样以编程方式添加自定义制表位。
System::SharedPtr<Aspose::Words::TabStopCollection> tabStops = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_TabStops();
tabStops->Add(72, Aspose::Words::TabAlignment::Left, Aspose::Words::TabLeader::Dots);
tabStops->Add(216, Aspose::Words::TabAlignment::Center, Aspose::Words::TabLeader::Dashes);
tabStops->Add(360, Aspose::Words::TabAlignment::Right, Aspose::Words::TabLeader::Line);

// 我们可以通过在 Microsoft Word 中通过 “View” -> “Show” -> “Ruler” 启用标尺来查看这些制表位。
ASSERT_EQ(3, para->GetEffectiveTabStops()->get_Length());

// 我们添加的任何制表符都会使用标尺上的制表位，并可能，
// 根据制表导线的值，在制表起点和终点之间留下空白。
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"\tTab 1\tTab 2\tTab 3"));

doc->Save(get_ArtifactsDir() + u"Paragraph.TabStops.docx");
```

## 另见

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
