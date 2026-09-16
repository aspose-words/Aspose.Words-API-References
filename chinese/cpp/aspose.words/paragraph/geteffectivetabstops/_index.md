---
title: "Aspose::Words::Paragraph::GetEffectiveTabStops method"
linktitle: "GetEffectiveTabStops"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Paragraph::GetEffectiveTabStops 方法。返回应用于此段落的所有制表位的数组，包括通过样式或列表间接应用的制表位（C++）。"
type: docs
weight: 26000
url: /zh/cpp/aspose.words/paragraph/geteffectivetabstops/
---
## Paragraph::GetEffectiveTabStops method


返回应用于此段落的所有制表位数组，包括通过样式或列表间接应用的制表位。

```cpp
System::ArrayPtr<System::SharedPtr<Aspose::Words::TabStop>> Aspose::Words::Paragraph::GetEffectiveTabStops()
```


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

* Class [TabStop](../../tabstop/)
* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
