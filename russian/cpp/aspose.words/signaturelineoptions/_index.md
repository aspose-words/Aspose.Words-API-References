---
title: "Aspose::Words::SignatureLineOptions class"
linktitle: "SignatureLineOptions"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::SignatureLineOptions class. Позволяет задавать параметры для вставляемой строки подписи. Используется в DocumentBuilder. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 61000
url: /ru/cpp/aspose.words/signaturelineoptions/
---
## SignatureLineOptions class


Позволяет задавать параметры для вставляемой строки подписи. Используется в [DocumentBuilder](../documentbuilder/). Чтобы узнать больше, посетите статью документации [Work with Digital Signatures](https://docs.aspose.com/words/cpp/working-with-digital-signatures/).

```cpp
class SignatureLineOptions : public System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_AllowComments](./get_allowcomments/)() const | Получает или задаёт значение, указывающее, что подписант может добавлять комментарии в диалоговом окне Sign. Значение свойства по умолчанию — **false**. |
| [get_DefaultInstructions](./get_defaultinstructions/)() const | Получает или задает значение, указывающее, что стандартные инструкции отображаются в диалоговом окне подписи. Значение по умолчанию для этого свойства — **true**. |
| [get_Email](./get_email/)() const | Получает или задает предложенный адрес электронной почты подписанта. Значение по умолчанию для этого свойства — **empty string**. |
| [get_Instructions](./get_instructions/)() const | Получает или задает инструкции подписанту, которые отображаются при подписании строки подписи. Значение по умолчанию для этого свойства — **empty string**. |
| [get_ShowDate](./get_showdate/)() const | Получает или задает значение, указывающее, что дата подписи отображается в строке подписи. Значение по умолчанию для этого свойства — **true**. |
| [get_Signer](./get_signer/)() const | Получает предложенного подписанта строки подписи. Значение по умолчанию для этого свойства — **empty string**. |
| [get_SignerTitle](./get_signertitle/)() const | Получает предложенную должность подписанта. Значение по умолчанию для этого свойства — **empty string**. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AllowComments](./set_allowcomments/)(bool) | Сеттер для [Aspose::Words::SignatureLineOptions::get_AllowComments](./get_allowcomments/). |
| [set_DefaultInstructions](./set_defaultinstructions/)(bool) | Сеттер для [Aspose::Words::SignatureLineOptions::get_DefaultInstructions](./get_defaultinstructions/). |
| [set_Email](./set_email/)(const System::String\&) | Сеттер для [Aspose::Words::SignatureLineOptions::get_Email](./get_email/). |
| [set_Instructions](./set_instructions/)(const System::String\&) | Сеттер для [Aspose::Words::SignatureLineOptions::get_Instructions](./get_instructions/). |
| [set_ShowDate](./set_showdate/)(bool) | Сеттер для [Aspose::Words::SignatureLineOptions::get_ShowDate](./get_showdate/). |
| [set_Signer](./set_signer/)(const System::String\&) | Устанавливает предложенного подписанта строки подписи. Значение по умолчанию для этого свойства — **empty string**. |
| [set_SignerTitle](./set_signertitle/)(const System::String\&) | Устанавливает предложенную должность подписанта. Значение по умолчанию для этого свойства — **empty string**. |
| [SignatureLineOptions](./signaturelineoptions/)() |  |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
