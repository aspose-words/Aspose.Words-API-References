---
title: "Aspose::Words::Drawing::ShapeBase::get_ParentParagraph method"
linktitle: "get_ParentParagraph"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::ShapeBase::get_ParentParagraph 方法。返回 C++ 中的直接父段落。"
type: docs
weight: 41000
url: /zh/cpp/aspose.words.drawing/shapebase/get_parentparagraph/
---
## ShapeBase::get_ParentParagraph method


返回直接父段落。

```cpp
System::SharedPtr<Aspose::Words::Paragraph> Aspose::Words::Drawing::ShapeBase::get_ParentParagraph()
```


## 示例



展示如何插入文本框，并设置其内容的字体。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 300, 50);
builder->MoveTo(shape->get_LastParagraph());
builder->Write(u"This text is inside the text box.");

// 将形状的 "Font" 对象的 "Hidden" 属性设置为 "true"，以隐藏文本框。
// 并折叠它通常占用的空间。
// 将形状的 "Font" 对象的 "Hidden" 属性设置为 "false"，使文本框保持可见。
shape->get_Font()->set_Hidden(hideShape);

// 如果形状可见，我们将通过字体对象修改其外观。
if (!hideShape)
{
    shape->get_Font()->set_HighlightColor(System::Drawing::Color::get_LightGray());
    shape->get_Font()->set_Color(System::Drawing::Color::get_Red());
    shape->get_Font()->set_Underline(Aspose::Words::Underline::Dash);
}

// 将构建器从文本框移回主文档。
builder->MoveTo(shape->get_ParentParagraph());

builder->Writeln(u"\nThis text is outside the text box.");

doc->Save(get_ArtifactsDir() + u"Shape.Font.docx");
```

## 另见

* Class [Paragraph](../../../aspose.words/paragraph/)
* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
