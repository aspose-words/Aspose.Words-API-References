---
title: "طريقة Aspose::Words::ParagraphFormat::get_CharacterUnitLeftIndent"
linktitle: "get_CharacterUnitLeftIndent"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::ParagraphFormat::get_CharacterUnitLeftIndent. يحصل أو يضبط قيمة المسافة اليسرى (بالحروف) للفقرات المحددة في C++."
type: docs
weight: 9000
url: /ar/cpp/aspose.words/paragraphformat/get_characterunitleftindent/
---
## ParagraphFormat::get_CharacterUnitLeftIndent method


يحصل أو يضبط قيمة المسافة البادئة اليسرى (بالحروف) للفقرات المحددة.

```cpp
double Aspose::Words::ParagraphFormat::get_CharacterUnitLeftIndent()
```


## أمثلة



يظهر كيفية تغيير تباعد الفقرات والمسافات البادئة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::ParagraphFormat> format = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat();

// فيما يلي خمسة خيارات تباعد مختلفة، إلى جانب الخصائص التي تؤثر على تكوينها بشكل غير مباشر.
// 1 -  المسافة اليسرى:
ASPOSE_ASSERT_EQ(format->get_LeftIndent(), 0.0);

format->set_CharacterUnitLeftIndent(10.0);

ASPOSE_ASSERT_EQ(format->get_LeftIndent(), 120.0);

// 2 -  المسافة اليمنى:
ASPOSE_ASSERT_EQ(format->get_RightIndent(), 0.0);

format->set_CharacterUnitRightIndent(-5.5);

ASPOSE_ASSERT_EQ(format->get_RightIndent(), -66.0);

// 3 -  المسافة المتدلية:
ASPOSE_ASSERT_EQ(format->get_FirstLineIndent(), 0.0);

format->set_CharacterUnitFirstLineIndent(20.3);

ASSERT_NEAR(format->get_FirstLineIndent(), 243.59, 0.1);

// 4 -  تباعد السطر قبل الفقرات:
ASPOSE_ASSERT_EQ(format->get_SpaceBefore(), 0.0);

format->set_LineUnitBefore(5.1);

ASSERT_NEAR(format->get_SpaceBefore(), 61.1, 0.1);

// 5 -  تباعد السطر بعد الفقرات:
ASPOSE_ASSERT_EQ(format->get_SpaceAfter(), 0.0);

format->set_LineUnitAfter(10.9);

ASSERT_NEAR(format->get_SpaceAfter(), 130.8, 0.1);

builder->Writeln(System::String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, ") + u"sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
builder->Write(System::String(u"测试文档测试文档测试文档测试文档测试文档测试文档测试文档测试文档测试") + u"文档测试文档测试文档测试文档测试文档测试文档测试文档测试文档测试文档测试文档");
```

## انظر أيضًا

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
