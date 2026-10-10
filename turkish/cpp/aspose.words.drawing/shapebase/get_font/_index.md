---
title: "Aspose::Words::Drawing::ShapeBase::get_Font yöntemi"
linktitle: "get_Font"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::ShapeBase::get_Font yöntemi. Bu nesnenin yazı tipi biçimlendirmesine erişim sağlar C++'da."
type: docs
weight: 21000
url: /tr/cpp/aspose.words.drawing/shapebase/get_font/
---
## ShapeBase::get_Font method


Bu nesnenin yazı tipi biçimlendirmesine erişim sağlar.

```cpp
System::SharedPtr<Aspose::Words::Font> Aspose::Words::Drawing::ShapeBase::get_Font()
```


## Örnekler



Bir metin kutusu eklemeyi ve içeriğinin yazı tipini ayarlamayı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 300, 50);
builder->MoveTo(shape->get_LastParagraph());
builder->Write(u"This text is inside the text box.");

// Şeklin "Font" nesnesinin "Hidden" özelliğini "true" olarak ayarlayarak metin kutusunu gizleyin.
// ve normalde kaplayacağı boşluğu daraltın.
// Şeklin "Font" nesnesinin "Hidden" özelliğini "false" olarak ayarlayarak metin kutusunun görünür kalmasını sağlayın.
shape->get_Font()->set_Hidden(hideShape);

// Şekil görünürse, görünümünü font nesnesi aracılığıyla değiştireceğiz.
if (!hideShape)
{
    shape->get_Font()->set_HighlightColor(System::Drawing::Color::get_LightGray());
    shape->get_Font()->set_Color(System::Drawing::Color::get_Red());
    shape->get_Font()->set_Underline(Aspose::Words::Underline::Dash);
}

// Builder'ı metin kutusundan çıkarıp ana belgeye geri taşıyın.
builder->MoveTo(shape->get_ParentParagraph());

builder->Writeln(u"\nThis text is outside the text box.");

doc->Save(get_ArtifactsDir() + u"Shape.Font.docx");
```

## Ayrıca Bakınız

* Class [Font](../../../aspose.words/font/)
* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
