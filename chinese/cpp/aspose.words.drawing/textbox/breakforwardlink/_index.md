---
title: "Aspose::Words::Drawing::TextBox::BreakForwardLink 方法"
linktitle: "BreakForwardLink"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::TextBox::BreakForwardLink 方法。断开与下一个 TextBox 的链接（C++）。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.drawing/textbox/breakforwardlink/
---
## TextBox::BreakForwardLink method


断开与下一个 [TextBox](../) 的链接。

```cpp
void Aspose::Words::Drawing::TextBox::BreakForwardLink()
```


## 示例



展示如何链接文本框。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> textBoxShape1 = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 100, 100);
System::SharedPtr<Aspose::Words::Drawing::TextBox> textBox1 = textBoxShape1->get_TextBox();
builder->Writeln();

System::SharedPtr<Aspose::Words::Drawing::Shape> textBoxShape2 = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 100, 100);
System::SharedPtr<Aspose::Words::Drawing::TextBox> textBox2 = textBoxShape2->get_TextBox();
builder->Writeln();

System::SharedPtr<Aspose::Words::Drawing::Shape> textBoxShape3 = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 100, 100);
System::SharedPtr<Aspose::Words::Drawing::TextBox> textBox3 = textBoxShape3->get_TextBox();
builder->Writeln();

System::SharedPtr<Aspose::Words::Drawing::Shape> textBoxShape4 = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 100, 100);
System::SharedPtr<Aspose::Words::Drawing::TextBox> textBox4 = textBoxShape4->get_TextBox();

// 在某些文本框之间创建链接。
if (textBox1->IsValidLinkTarget(textBox2))
{
    textBox1->set_Next(textBox2);
}

if (textBox2->IsValidLinkTarget(textBox3))
{
    textBox2->set_Next(textBox3);
}

// 只有空的文本框才能拥有链接。
ASSERT_TRUE(textBox3->IsValidLinkTarget(textBox4));

builder->MoveTo(textBoxShape4->get_LastParagraph());
builder->Write(u"Hello world!");

ASSERT_FALSE(textBox3->IsValidLinkTarget(textBox4));

if (textBox1->get_Next() != nullptr && textBox1->get_Previous() == nullptr)
{
    std::cout << "This TextBox is the head of the sequence" << std::endl;
}

if (textBox2->get_Next() != nullptr && textBox2->get_Previous() != nullptr)
{
    std::cout << "This TextBox is the middle of the sequence" << std::endl;
}

if (textBox3->get_Next() == nullptr && textBox3->get_Previous() != nullptr)
{
    std::cout << "This TextBox is the tail of the sequence" << std::endl;

    // 断开 textBox2 与 textBox3 之间的前向链接，然后验证它们不再链接。
    textBox3->get_Previous()->BreakForwardLink();
    ASSERT_TRUE(textBox2->get_Next() == nullptr);
    ASSERT_TRUE(textBox3->get_Previous() == nullptr);
}

doc->Save(get_ArtifactsDir() + u"Shape.CreateLinkBetweenTextBoxes.docx");
```

## 另见

* Class [TextBox](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
