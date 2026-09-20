---
title: "Aspose::Words::DocumentBuilder::InsertSignatureLine метод"
linktitle: "InsertSignatureLine"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::DocumentBuilder::InsertSignatureLine метод. Вставляет строку подписи в текущую позицию на C++."
type: docs
weight: 46000
url: /ru/cpp/aspose.words/documentbuilder/insertsignatureline/
---
## DocumentBuilder::InsertSignatureLine(const System::SharedPtr\<Aspose::Words::SignatureLineOptions\>\&) method


Вставляет строку подписи в текущую позицию.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertSignatureLine(const System::SharedPtr<Aspose::Words::SignatureLineOptions> &signatureLineOptions)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| signatureLineOptions | const System::SharedPtr\<Aspose::Words::SignatureLineOptions\>\& | Объект, который хранит параметры создания строки подписи. |

### ReturnValue

Узел строки подписи, который только что был вставлен.

## Примеры



Показывает, как подписать документ с помощью личного сертификата и строки подписи.
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

// Снова откройте сохранённый документ и убедитесь, что свойства "IsSigned" и "IsValid" оба равны "true",
// что указывает на наличие подписи в строке подписи.
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"DocumentBuilder.SignatureLineProviderId.Signed.docx");
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
signatureLine = shape->get_SignatureLine();

ASSERT_TRUE(signatureLine->get_IsSigned());
ASSERT_TRUE(signatureLine->get_IsValid());
```

## См. также

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [SignatureLineOptions](../../signaturelineoptions/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertSignatureLine(const System::SharedPtr\<Aspose::Words::SignatureLineOptions\>\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, Aspose::Words::Drawing::WrapType) method


Вставляет строку подписи в указанную позицию.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertSignatureLine(const System::SharedPtr<Aspose::Words::SignatureLineOptions> &signatureLineOptions, Aspose::Words::Drawing::RelativeHorizontalPosition horzPos, double left, Aspose::Words::Drawing::RelativeVerticalPosition vertPos, double top, Aspose::Words::Drawing::WrapType wrapType)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| signatureLineOptions | const System::SharedPtr\<Aspose::Words::SignatureLineOptions\>\& | Объект, который хранит параметры создания строки подписи. |
| horzPos | Aspose::Words::Drawing::RelativeHorizontalPosition | Указывает, откуда измеряется расстояние до строки подписи. |
| left | double | Расстояние в пунктах от начала координат до левой стороны строки подписи. |
| vertPos | Aspose::Words::Drawing::RelativeVerticalPosition | Указывает, откуда измеряется расстояние до строки подписи. |
| top | double | Расстояние в пунктах от начала координат до верхней стороны строки подписи. |
| wrapType | Aspose::Words::Drawing::WrapType | Указывает, как обтекать текст вокруг строки подписи. |

### ReturnValue

Узел строки подписи, который только что был вставлен.
## Примечания


Вы можете изменить размер изображения, его расположение, способ позиционирования и другие параметры, используя объект [Shape](../../../aspose.words.drawing/shape/), возвращаемый этим методом.

## Примеры



Показывает, как вставить встроенную строку подписи в документ.
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

// Строку подписи можно подписать в Microsoft Word, дважды щёлкнув по ней.
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.SignatureLineInline.docx");
```

## См. также

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [SignatureLineOptions](../../signaturelineoptions/)
* Enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* Enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* Enum [WrapType](../../../aspose.words.drawing/wraptype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
