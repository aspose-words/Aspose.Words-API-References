---
title: "Aspose::Words::ParagraphFormat::get_CharacterUnitFirstLineIndent method"
linktitle: "get_CharacterUnitFirstLineIndent"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::ParagraphFormat::get_CharacterUnitFirstLineIndent method. 获取或设置首行或悬挂缩进的值（以字符为单位）。使用正值设置首行缩进，使用负值设置悬挂缩进（C++）。"
type: docs
weight: 8000
url: /zh/cpp/aspose.words/paragraphformat/get_characterunitfirstlineindent/
---
## ParagraphFormat::get_CharacterUnitFirstLineIndent method


获取或设置首行缩进或悬挂缩进的值（以字符为单位）。使用正值设置首行缩进，使用负值设置悬挂缩进。

```cpp
double Aspose::Words::ParagraphFormat::get_CharacterUnitFirstLineIndent()
```


## 示例



展示如何更改段落间距和缩进。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::ParagraphFormat> format = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat();

// 以下是五种不同的间距选项，以及其配置间接影响的属性。
// 1 -  左缩进：
ASPOSE_ASSERT_EQ(format->get_LeftIndent(), 0.0);

format->set_CharacterUnitLeftIndent(10.0);

ASPOSE_ASSERT_EQ(format->get_LeftIndent(), 120.0);

// 2 -  右缩进：
ASPOSE_ASSERT_EQ(format->get_RightIndent(), 0.0);

format->set_CharacterUnitRightIndent(-5.5);

ASPOSE_ASSERT_EQ(format->get_RightIndent(), -66.0);

// 3 -  悬挂缩进：
ASPOSE_ASSERT_EQ(format->get_FirstLineIndent(), 0.0);

format->set_CharacterUnitFirstLineIndent(20.3);

ASSERT_NEAR(format->get_FirstLineIndent(), 243.59, 0.1);

// 4 -  段落前的行距：
ASPOSE_ASSERT_EQ(format->get_SpaceBefore(), 0.0);

format->set_LineUnitBefore(5.1);

ASSERT_NEAR(format->get_SpaceBefore(), 61.1, 0.1);

// 5 -  段落后的行距：
ASPOSE_ASSERT_EQ(format->get_SpaceAfter(), 0.0);

format->set_LineUnitAfter(10.9);

ASSERT_NEAR(format->get_SpaceAfter(), 130.8, 0.1);

builder->Writeln(System::String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, ") + u"sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
builder->Write(System::String(u"测试文档测试文档测试文档测试文档测试文档测试文档测试文档测试文档测试") + u"文档测试文档测试文档测试文档测试文档测试文档测试文档测试文档测试文档测试文档");
```

## 另见

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
