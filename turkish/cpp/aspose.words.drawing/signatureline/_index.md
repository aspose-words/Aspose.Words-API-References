---
title: "Aspose::Words::Drawing::SignatureLine class"
linktitle: "SignatureLine"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::SignatureLine class. İmza satırı özelliklerine erişim sağlar. Daha fazla bilgi için C++ belgelerindeki makaleyi ziyaret edin."
type: docs
weight: 13000
url: /tr/cpp/aspose.words.drawing/signatureline/
---
## SignatureLine class


İmza satırı özelliklerine erişim sağlar. Daha fazla bilgi edinmek için [Work with Digital Signatures](https://docs.aspose.com/words/cpp/working-with-digital-signatures/) dokümantasyon makalesini ziyaret edin.

```cpp
class SignatureLine : public System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get_AllowComments](./get_allowcomments/)() | İmzalayanın İmzala iletişim kutusunda yorum ekleyebileceğini belirten bir değeri alır veya ayarlar. Bu özelliğin varsayılan değeri **false**. |
| [get_DefaultInstructions](./get_defaultinstructions/)() | İmzalama iletişim kutusunda varsayılan talimatların gösterildiğini belirten bir değeri alır veya ayarlar. Bu özelliğin varsayılan değeri **true**. |
| [get_Email](./get_email/)() | Önerilen imzalayanın e-posta adresini alır veya ayarlar. Bu özelliğin varsayılan değeri **empty string**. |
| [get_Id](./get_id/)() | Bu imza satırı için tanımlayıcıyı alır veya ayarlar. Bu tanımlayıcı, belgeyi [DigitalSignatureUtil](../../aspose.words.digitalsignatures/digitalsignatureutil/) kullanarak imzalarken dijital imza ile ilişkilendirilebilir. Bu değer benzersiz olmalı ve varsayılan olarak rastgele oluşturulan yeni Guid (**NewGuid**) olur. |
| [get_Instructions](./get_instructions/)() | İmzalayan kişiye gösterilen talimatları alır veya ayarlar. Bu özellik, [DefaultInstructions](./get_defaultinstructions/) ayarlanmışsa yok sayılır. Bu özelliğin varsayılan değeri **empty string**. |
| [get_IsSigned](./get_issigned/)() | İmza satırının dijital imza ile imzalandığını gösterir. |
| [get_IsValid](./get_isvalid/)() | İmza satırının dijital imza ile imzalandığını ve bu dijital imzanın geçerli olduğunu gösterir. |
| [get_ProviderId](./get_providerid/)() | Bu imza satırı için imza sağlayıcı tanımlayıcısını alır veya ayarlar. Varsayılan değer "{00000000-0000-0000-0000-000000000000}". |
| [get_ShowDate](./get_showdate/)() | İmza satırında imza tarihinin gösterildiğini belirten bir değeri alır veya ayarlar. Bu özelliğin varsayılan değeri **true**. |
| [get_Signer](./get_signer/)() | İmza satırının önerilen imzalayanını alır veya ayarlar. Bu özelliğin varsayılan değeri **empty string**. |
| [get_SignerTitle](./get_signertitle/)() | Önerilen imzalayanın unvanını (örneğin, Manager) alır veya ayarlar. Bu özelliğin varsayılan değeri **empty string**. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AllowComments](./set_allowcomments/)(bool) | Ayarlayıcı [Aspose::Words::Drawing::SignatureLine::get_AllowComments](./get_allowcomments/). |
| [set_DefaultInstructions](./set_defaultinstructions/)(bool) | Ayarlayıcı [Aspose::Words::Drawing::SignatureLine::get_DefaultInstructions](./get_defaultinstructions/). |
| [set_Email](./set_email/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Drawing::SignatureLine::get_Email](./get_email/). |
| [set_Id](./set_id/)(System::Guid) | Ayarlayıcı [Aspose::Words::Drawing::SignatureLine::get_Id](./get_id/). |
| [set_Instructions](./set_instructions/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Drawing::SignatureLine::get_Instructions](./get_instructions/). |
| [set_ProviderId](./set_providerid/)(System::Guid) | Ayarlayıcı [Aspose::Words::Drawing::SignatureLine::get_ProviderId](./get_providerid/). |
| [set_ShowDate](./set_showdate/)(bool) | Ayarlayıcı [Aspose::Words::Drawing::SignatureLine::get_ShowDate](./get_showdate/). |
| [set_Signer](./set_signer/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Drawing::SignatureLine::get_Signer](./get_signer/). |
| [set_SignerTitle](./set_signertitle/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Drawing::SignatureLine::get_SignerTitle](./get_signertitle/). |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
