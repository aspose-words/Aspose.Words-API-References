---
title: "طريقة Aspose::Words::Drawing::ShapeBase::get_ParentParagraph"
linktitle: "get_ParentParagraph"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Drawing::ShapeBase::get_ParentParagraph. تُرجع الفقرة الأصلية المباشرة في C++."
type: docs
weight: 41000
url: /ar/cpp/aspose.words.drawing/shapebase/get_parentparagraph/
---
## ShapeBase::get_ParentParagraph method


إرجاع الفقرة الأصلية المباشرة.

```cpp
System::SharedPtr<Aspose::Words::Paragraph> Aspose::Words::Drawing::ShapeBase::get_ParentParagraph()
```


## أمثلة



يوضح كيفية إدراج مربع نص وتعيين خط محتوياته.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 300, 50);
builder->MoveTo(shape->get_LastParagraph());
builder->Write(u"This text is inside the text box.");

// اضبط خاصية "Hidden" لكائن "Font" الخاص بالشكل إلى "true" لإخفاء مربع النص عن الأنظار
// واقلص المساحة التي كان سيشغلها عادةً.
// اضبط خاصية "Hidden" لكائن "Font" الخاص بالشكل إلى "false" لجعل مربع النص مرئياً.
shape->get_Font()->set_Hidden(hideShape);

// إذا كان الشكل مرئياً، سنقوم بتعديل مظهره عبر كائن الخط.
if (!hideShape)
{
    shape->get_Font()->set_HighlightColor(System::Drawing::Color::get_LightGray());
    shape->get_Font()->set_Color(System::Drawing::Color::get_Red());
    shape->get_Font()->set_Underline(Aspose::Words::Underline::Dash);
}

// انقل المُنشئ خارج مربع النص عائدًا إلى المستند الرئيسي.
builder->MoveTo(shape->get_ParentParagraph());

builder->Writeln(u"\nThis text is outside the text box.");

doc->Save(get_ArtifactsDir() + u"Shape.Font.docx");
```

## انظر أيضًا

* Class [Paragraph](../../../aspose.words/paragraph/)
* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
