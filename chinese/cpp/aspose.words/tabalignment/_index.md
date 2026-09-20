---
title: "Aspose::Words::TabAlignment 枚举"
linktitle: "TabAlignment"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::TabAlignment 枚举。指定 C++ 中制表位的对齐方式/类型。"
type: docs
weight: 120000
url: /zh/cpp/aspose.words/tabalignment/
---
## TabAlignment enum


指定制表位的对齐方式/类型。

```cpp
enum class TabAlignment
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| 左 | 0 | 将制表位后的文本左对齐。 |
| 居中 | 1 | 将文本居中于制表位。 |
| 右 | 2 | 将文本右对齐于制表位。 |
| Decimal | 3 | 将文本对齐到小数点。 |
| Bar | 4 | 在制表位位置绘制垂直条。 |
| 列表 | 6 | 制表位是列表项中数字/项目符号与文本之间的分隔符。 |
| 清除 | 7 | 清除此位置的所有制表位。 |


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
