---
title: "Aspose::Words::DocumentBuilder::InsertSignatureLine metodu"
linktitle: "InsertSignatureLine"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::DocumentBuilder::InsertSignatureLine metodu. C++'ta geçerli konuma bir imza satırı ekler."
type: docs
weight: 46000
url: /tr/cpp/aspose.words/documentbuilder/insertsignatureline/
---
## DocumentBuilder::InsertSignatureLine(const System::SharedPtr\<Aspose::Words::SignatureLineOptions\>\&) method


Geçerli konuma bir imza satırı ekler.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertSignatureLine(const System::SharedPtr<Aspose::Words::SignatureLineOptions> &signatureLineOptions)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| signatureLineOptions | const System::SharedPtr\<Aspose::Words::SignatureLineOptions\>\& | İmza satırı oluşturma parametrelerini depolayan nesne. |

### ReturnValue

Az önce eklenen imza satırı düğümü.

## Örnekler



Kişisel bir sertifika ve imza satırıyla bir belgeyi nasıl imzalayacağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto signatureLineOptions = System::MakeObject<Aspose::Words::SignatureLineOptions>();
signatureLineOptions->set_Signer(u"vderyushev");
signatureLineOptions->set_SignerTitle(u"QA");
signatureLineOptions->set_Email(u"vderyushev@aspose.com");
signatureLineOptions->set_ShowDate(true);
signatureLineOptions->set_DefaultInstructions(false);
signatureLineOptions->set_Instructions(u"Please sign here.");
signatureLineOptions->set_AllowComments(true);

System::SharedPtr<Aspose::Words::Drawing::SignatureLine> signatureLine = builder->InsertSignatureLine(signatureLineOptions)->get_SignatureLine();
signatureLine->set_ProviderId(System::Guid::Parse(u"CF5A7BB4-8F3C-4756-9DF6-BEF7F13259A2"));

ASSERT_FALSE(signatureLine->get_IsSigned());
ASSERT_FALSE(signatureLine->get_IsValid());

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.SignatureLineProviderId.docx");

auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_SignatureLineId(signatureLine->get_Id());
signOptions->set_ProviderId(signatureLine->get_ProviderId());
signOptions->set_Comments(u"Document was signed by vderyushev");
signOptions->set_SignTime(System::DateTime::get_Now());

System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certHolder = Aspose::Words::DigitalSignatures::CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw");

Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(get_ArtifactsDir() + u"DocumentBuilder.SignatureLineProviderId.docx", get_ArtifactsDir() + u"DocumentBuilder.SignatureLineProviderId.Signed.docx", certHolder, signOptions);

// Kaydedilmiş belgemizi yeniden açın ve "IsSigned" ve "IsValid" özelliklerinin her ikisinin de "true" olduğunu doğrulayın,
// bu, imza satırının bir imza içerdiğini gösterir.
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"DocumentBuilder.SignatureLineProviderId.Signed.docx");
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
signatureLine = shape->get_SignatureLine();

ASSERT_TRUE(signatureLine->get_IsSigned());
ASSERT_TRUE(signatureLine->get_IsValid());
```

## Ayrıca Bakınız

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [SignatureLineOptions](../../signaturelineoptions/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertSignatureLine(const System::SharedPtr\<Aspose::Words::SignatureLineOptions\>\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, Aspose::Words::Drawing::WrapType) method


Belirtilen konuma bir imza satırı ekler.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertSignatureLine(const System::SharedPtr<Aspose::Words::SignatureLineOptions> &signatureLineOptions, Aspose::Words::Drawing::RelativeHorizontalPosition horzPos, double left, Aspose::Words::Drawing::RelativeVerticalPosition vertPos, double top, Aspose::Words::Drawing::WrapType wrapType)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| signatureLineOptions | const System::SharedPtr\<Aspose::Words::SignatureLineOptions\>\& | İmza satırı oluşturma parametrelerini depolayan nesne. |
| horzPos | Aspose::Words::Drawing::RelativeHorizontalPosition | İmza satırına olan mesafenin ölçüldüğü yeri belirtir. |
| left | double | Köken noktasından imza satırının sol tarafına kadar olan mesafe (nokta cinsinden). |
| vertPos | Aspose::Words::Drawing::RelativeVerticalPosition | İmza satırına olan mesafenin ölçüldüğü yeri belirtir. |
| üst | double | Köken noktasından imza satırının üst tarafına kadar olan mesafe (nokta cinsinden). |
| wrapType | Aspose::Words::Drawing::WrapType | Metnin imza satırının etrafında nasıl kaydırılacağını belirtir. |

### ReturnValue

Az önce eklenen imza satırı düğümü.
## Açıklamalar


Bu metodun döndürdüğü [Shape](../../../aspose.words.drawing/shape/) nesnesini kullanarak görüntü boyutunu, konumunu, konumlandırma yöntemini ve diğer ayarları değiştirebilirsiniz.

## Örnekler



Bir belgeye satır içi imza satırı eklemenin nasıl yapılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto options = System::MakeObject<Aspose::Words::SignatureLineOptions>();
options->set_Signer(u"John Doe");
options->set_SignerTitle(u"Manager");
options->set_Email(u"johndoe@aspose.com");
options->set_ShowDate(true);
options->set_DefaultInstructions(false);
options->set_Instructions(u"Please sign here.");
options->set_AllowComments(true);

builder->InsertSignatureLine(options, Aspose::Words::Drawing::RelativeHorizontalPosition::RightMargin, 2.0, Aspose::Words::Drawing::RelativeVerticalPosition::Page, 3.0, Aspose::Words::Drawing::WrapType::Inline);

// İmza satırı, Microsoft Word'de üzerine çift tıklanarak imzalanabilir.
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.SignatureLineInline.docx");
```

## Ayrıca Bakınız

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [SignatureLineOptions](../../signaturelineoptions/)
* Enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* Enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* Enum [WrapType](../../../aspose.words.drawing/wraptype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
