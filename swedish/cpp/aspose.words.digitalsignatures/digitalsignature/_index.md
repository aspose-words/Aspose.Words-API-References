---
title: "Aspose::Words::DigitalSignatures::DigitalSignature-klass"
linktitle: "DigitalSignature"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::DigitalSignatures::DigitalSignature-klass. Representerar en digital signatur på ett dokument och resultatet av dess verifiering. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words.digitalsignatures/digitalsignature/
---
## DigitalSignature class


Representerar en digital signatur i ett dokument och resultatet av dess verifiering. För att lära dig mer, besök artikeln [Work with Digital Signatures](https://docs.aspose.com/words/cpp/working-with-digital-signatures/) documentation article.

```cpp
class DigitalSignature : public System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [get_ApplicationVersion](./get_applicationversion/)() | Hämtar applikationsversionen för den digitala signaturen. |
| [get_CertificateHolder](./get_certificateholder/)() const | Returnerar certifikathållarobjektet som innehåller certifikatet som användes för att signera dokumentet. |
| [get_ColorDepth](./get_colordepth/)() | Hämtar färgdjupet för den digitala signaturen. |
| [get_Comments](./get_comments/)() | Hämtar kommentaren för signeringsändamålet. |
| [get_HorizontalResolution](./get_horizontalresolution/)() | Hämtar den horisontella upplösningen för den digitala signaturen. |
| [get_IssuerName](./get_issuername/)() | Returnerar den ämnessärskilda namnet för certifikatutfärdaren. |
| [get_IsValid](./get_isvalid/)() const | Returnerar **true** om denna digitala signatur är giltig och dokumentet inte har manipulerats. |
| [get_OfficeVersion](./get_officeversion/)() | Hämtar Office-versionen för den digitala signaturen. |
| [get_SignatureType](./get_signaturetype/)() const | Hämtar typen av den digitala signaturen. |
| [get_SignatureValue](./get_signaturevalue/)() const | Hämtar en bytearray som representerar ett signaturvärde. |
| [get_SignTime](./get_signtime/)() const | Hämtar tiden då dokumentet signerades. |
| [get_SubjectName](./get_subjectname/)() | Returnerar det ämnessärskilda namnet för certifikatet som användes för att signera dokumentet. |
| [get_VerticalResolution](./get_verticalresolution/)() | Hämtar den vertikala upplösningen för den digitala signaturen. |
| [get_WindowsVersion](./get_windowsversion/)() | Hämtar Windows-versionen för den digitala signaturen. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [ToString](./tostring/)() const override | Returnerar en användarvänlig sträng som visar värdet för detta objekt. |
| static [Type](./type/)() |  |

## Exempel



Visar hur man validerar och visar information om varje signatur i ett dokument.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Digitally signed.docx");

for (auto&& signature : doc->get_DigitalSignatures())
{
    std::cout << System::String::Format(u"{0} signature: ", (signature->get_IsValid() ? System::String(u"Valid") : System::String(u"Invalid"))) << std::endl;
    std::cout << System::String::Format(u"\tReason:\t{0}", signature->get_Comments()) << std::endl;
    std::cout << System::String::Format(u"\tType:\t{0}", signature->get_SignatureType()) << std::endl;
    std::cout << System::String::Format(u"\tSign time:\t{0}", signature->get_SignTime()) << std::endl;
    std::cout << System::String::Format(u"\tSubject name:\t{0}", signature->get_CertificateHolder()->get_Certificate()->get_SubjectName()) << std::endl;
    std::cout << System::String::Format(u"\tIssuer name:\t{0}", signature->get_CertificateHolder()->get_Certificate()->get_IssuerName()->get_Name()) << std::endl;
    std::cout << std::endl;
}
```

## Se även

* Namespace [Aspose::Words::DigitalSignatures](../)
* Library [Aspose.Words for C++](../../)
