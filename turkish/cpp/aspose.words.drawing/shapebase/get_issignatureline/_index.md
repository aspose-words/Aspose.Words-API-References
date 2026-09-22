---
title: "Aspose::Words::Drawing::ShapeBase::get_IsSignatureLine metodu"
linktitle: "get_IsSignatureLine"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::ShapeBase::get_IsSignatureLine metodu. Şeklin C++'ta bir SignatureLine olduğunu gösterir."
type: docs
weight: 35000
url: /tr/cpp/aspose.words.drawing/shapebase/get_issignatureline/
---
## ShapeBase::get_IsSignatureLine method


Şeklin bir [SignatureLine](../../signatureline/) olduğunu gösterir.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_IsSignatureLine()
```


## Örnekler



Bir imza satırı oluşturmayı ve belgeye eklemeyi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto options = System::MakeObject<Aspose::Words::SignatureLineOptions>();
options->set_AllowComments(true);
options->set_DefaultInstructions(true);
options->set_Email(u"john.doe@management.com");
options->set_Instructions(u"Please sign here");
options->set_ShowDate(true);
options->set_Signer(u"John Doe");
options->set_SignerTitle(u"Senior Manager");

// İmza satırını içerecek bir şekil ekleyin, görünümünü
// yukarıda oluşturduğumuz "SignatureLineOptions" nesnesini kullanarak özelleştirin.
// Eğer bir şeklin koordinatları sayfanın sağ alt köşesinden başlıyorsa,
// şekli görünür hâle getirmek için negatif x ve y koordinatları sağlamamız gerekir.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertSignatureLine(options, Aspose::Words::Drawing::RelativeHorizontalPosition::RightMargin, -170.0, Aspose::Words::Drawing::RelativeVerticalPosition::BottomMargin, -60.0, Aspose::Words::Drawing::WrapType::None);

ASSERT_TRUE(shape->get_IsSignatureLine());

// İmza satırımızın özelliklerini Shape nesnesi aracılığıyla doğrulayın.
System::SharedPtr<Aspose::Words::Drawing::SignatureLine> signatureLine = shape->get_SignatureLine();

ASSERT_EQ(u"john.doe@management.com", signatureLine->get_Email());
ASSERT_EQ(u"John Doe", signatureLine->get_Signer());
ASSERT_EQ(u"Senior Manager", signatureLine->get_SignerTitle());
ASSERT_EQ(u"Please sign here", signatureLine->get_Instructions());
ASSERT_TRUE(signatureLine->get_ShowDate());
ASSERT_TRUE(signatureLine->get_AllowComments());
ASSERT_TRUE(signatureLine->get_DefaultInstructions());

doc->Save(get_ArtifactsDir() + u"Shape.SignatureLine.docx");
```

## Ayrıca Bakınız

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
