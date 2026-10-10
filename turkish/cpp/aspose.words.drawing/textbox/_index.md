---
title: "Aspose::Words::Drawing::TextBox class"
linktitle: "MetinKutusu"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::TextBox class. Bir şekil içinde metnin nasıl görüntüleneceğini belirten öznitelikleri tanımlar. Daha fazla bilgi edinmek için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 15000
url: /tr/cpp/aspose.words.drawing/textbox/
---
## TextBox class


Bir şekil içinde metnin nasıl görüntüleneceğini belirten öznitelikleri tanımlar. Daha fazla bilgi edinmek için [Working with Shapes](https://docs.aspose.com/words/cpp/working-with-shapes/) dokümantasyon makalesini ziyaret edin.

```cpp
class TextBox : public System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [BreakForwardLink](./breakforwardlink/)() | Sonraki [TextBox](./) bağlantısını keser. |
| [get_FitShapeToText](./get_fitshapetotext/)() | Microsoft Word'ün şekli metne sığdırmak için büyütüp büyütmeyeceğini belirler. |
| [get_InternalMarginBottom](./get_internalmarginbottom/)() | Bir şekil için iç alt kenar boşluğunu puan cinsinden belirtir. |
| [get_InternalMarginLeft](./get_internalmarginleft/)() | Bir şekil için iç sol kenar boşluğunu puan cinsinden belirtir. |
| [get_InternalMarginRight](./get_internalmarginright/)() | Bir şekil için iç sağ kenar boşluğunu puan cinsinden belirtir. |
| [get_InternalMarginTop](./get_internalmargintop/)() | Bir şekil için iç üst kenar boşluğunu puan cinsinden belirtir. |
| [get_LayoutFlow](./get_layoutflow/)() | Bir şekil içinde metin düzeninin akışını belirler. |
| [get_Next](./get_next/)() | Şekil dizisinde bir sonraki [TextBox](./) öğesini temsil eden bir [TextBox](./) döndürür veya ayarlar. |
| [get_NoTextRotation](./get_notextrotation/)() | Şekil döndürüldüğünde [TextBox](./) metninin dönmemesi gerektiğini gösteren bir boolean değer alır veya ayarlar. |
| [get_Parent](./get_parent/)() const | [TextBox](./) için bir üst şekil alır. |
| [get_Previous](./get_previous/)() | Şekil dizisinde önceki [TextBox](./) öğesini temsil eden bir [TextBox](./) döndürür. |
| [get_TextBoxWrapMode](./get_textboxwrapmode/)() | Metnin bir şekil içinde nasıl kaydırılacağını belirler. |
| [get_VerticalAnchor](./get_verticalanchor/)() | Bir şekil içinde metnin dikey hizalamasını belirtir. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsValidLinkTarget](./isvalidlinktarget/)(const System::SharedPtr\<Aspose::Words::Drawing::TextBox\>\&) | Bu [TextBox](./) öğesinin hedef [TextBox](./) öğesine bağlanıp bağlanamayacağını belirler. |
| [set_FitShapeToText](./set_fitshapetotext/)(bool) | [Aspose::Words::Drawing::TextBox::get_FitShapeToText](./get_fitshapetotext/) için ayarlayıcı. |
| [set_InternalMarginBottom](./set_internalmarginbottom/)(double) | [Aspose::Words::Drawing::TextBox::get_InternalMarginBottom](./get_internalmarginbottom/) için ayarlayıcı. |
| [set_InternalMarginLeft](./set_internalmarginleft/)(double) | [Aspose::Words::Drawing::TextBox::get_InternalMarginLeft](./get_internalmarginleft/) için ayarlayıcı. |
| [set_InternalMarginRight](./set_internalmarginright/)(double) | [Aspose::Words::Drawing::TextBox::get_InternalMarginRight](./get_internalmarginright/) için ayarlayıcı. |
| [set_InternalMarginTop](./set_internalmargintop/)(double) | [Aspose::Words::Drawing::TextBox::get_InternalMarginTop](./get_internalmargintop/) için ayarlayıcı. |
| [set_LayoutFlow](./set_layoutflow/)(Aspose::Words::Drawing::LayoutFlow) | [Aspose::Words::Drawing::TextBox::get_LayoutFlow](./get_layoutflow/) için ayarlayıcı. |
| [set_Next](./set_next/)(const System::SharedPtr\<Aspose::Words::Drawing::TextBox\>\&) | [Aspose::Words::Drawing::TextBox::get_Next](./get_next/) için ayarlayıcı. |
| [set_NoTextRotation](./set_notextrotation/)(bool) | [Aspose::Words::Drawing::TextBox::get_NoTextRotation](./get_notextrotation/) için ayarlayıcı. |
| [set_TextBoxWrapMode](./set_textboxwrapmode/)(Aspose::Words::Drawing::TextBoxWrapMode) | [Aspose::Words::Drawing::TextBox::get_TextBoxWrapMode](./get_textboxwrapmode/) için ayarlayıcı. |
| [set_VerticalAnchor](./set_verticalanchor/)(Aspose::Words::Drawing::TextBoxAnchor) | [Aspose::Words::Drawing::TextBox::get_VerticalAnchor](./get_verticalanchor/) için ayarlayıcı. |
| static [Type](./type/)() |  |
## Açıklamalar


[TextBox](../shape/get_textbox/) özelliğini bir şeklin metin özelliklerine erişmek için kullanın. [TextBox](./) sınıfının örneklerini doğrudan oluşturmazsınız.

## Örnekler



Bir metin kutusunun içindeki metnin yönünü nasıl ayarlayacağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> textBoxShape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 150, 100);
System::SharedPtr<Aspose::Words::Drawing::TextBox> textBox = textBoxShape->get_TextBox();

// Belge oluşturucuyu TextBox içine taşıyın ve metin ekleyin.
builder->MoveTo(textBoxShape->get_LastParagraph());
builder->Writeln(u"Hello world!");
builder->Write(u"Hello again!");

// \"LayoutFlow\" özelliğini ayarlayarak bu metin kutusunun metin içeriği için bir yön belirleyin.
textBox->set_LayoutFlow(layoutFlow);

doc->Save(get_ArtifactsDir() + u"Shape.TextBoxLayoutFlow.docx");
```


Bir metin kutusunun içeriğine sıkı bir şekilde sığacak şekilde kendini yeniden boyutlandırmasını nasıl sağlayacağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> textBoxShape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 150, 100);
System::SharedPtr<Aspose::Words::Drawing::TextBox> textBox = textBoxShape->get_TextBox();

// Bu değerleri her iki üye için de uygulayarak üst şeklin sığmasını sağlayın
// metin içeriğinin etrafına sıkı bir şekilde, ayarladığımız boyutları göz ardı ederek.
textBox->set_FitShapeToText(true);
textBox->set_TextBoxWrapMode(Aspose::Words::Drawing::TextBoxWrapMode::None);

builder->MoveTo(textBoxShape->get_LastParagraph());
builder->Write(u"Text fit tightly inside textbox.");

doc->Save(get_ArtifactsDir() + u"Shape.TextBoxFitShapeToText.docx");
```


Bir metin kutusu için iç kenar boşluklarını nasıl ayarlayacağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Belirli kenar boşluklarına sahip başka bir metin kutusu ekleyin.
System::SharedPtr<Aspose::Words::Drawing::Shape> textBoxShape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 100, 100);
System::SharedPtr<Aspose::Words::Drawing::TextBox> textBox = textBoxShape->get_TextBox();
textBox->set_InternalMarginTop(15);
textBox->set_InternalMarginBottom(15);
textBox->set_InternalMarginLeft(15);
textBox->set_InternalMarginRight(15);

builder->MoveTo(textBoxShape->get_LastParagraph());
builder->Write(u"Text placed according to textbox margins.");

doc->Save(get_ArtifactsDir() + u"Shape.TextBoxMargins.docx");
```

## Ayrıca Bakınız

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
