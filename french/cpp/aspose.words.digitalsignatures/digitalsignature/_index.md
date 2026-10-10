---
title: "Aspose::Words::DigitalSignatures::DigitalSignature class"
linktitle: "DigitalSignature"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::DigitalSignatures::DigitalSignature class. Représente une signature numérique sur un document et le résultat de sa vérification. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words.digitalsignatures/digitalsignature/
---
## DigitalSignature class


Représente une signature numérique sur un document et le résultat de sa vérification. Pour en savoir plus, consultez l’article de documentation [Work with Digital Signatures](https://docs.aspose.com/words/cpp/working-with-digital-signatures/).

```cpp
class DigitalSignature : public System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [get_ApplicationVersion](./get_applicationversion/)() | Obtient la version de l'application pour la signature numérique. |
| [get_CertificateHolder](./get_certificateholder/)() const | Renvoie l'objet détenteur du certificat qui contient le certificat utilisé pour signer le document. |
| [get_ColorDepth](./get_colordepth/)() | Obtient la profondeur de couleur pour la signature numérique. |
| [get_Comments](./get_comments/)() | Obtient le commentaire de l'objectif de signature. |
| [get_HorizontalResolution](./get_horizontalresolution/)() | Obtient la résolution horizontale pour la signature numérique. |
| [get_IssuerName](./get_issuername/)() | Renvoie le nom distinctif du sujet du certificat émetteur. |
| [get_IsValid](./get_isvalid/)() const | Renvoie **true** si cette signature numérique est valide et que le document n'a pas été altéré. |
| [get_OfficeVersion](./get_officeversion/)() | Obtient la version Office pour la signature numérique. |
| [get_SignatureType](./get_signaturetype/)() const | Obtient le type de la signature numérique. |
| [get_SignatureValue](./get_signaturevalue/)() const | Obtient un tableau d'octets représentant une valeur de signature. |
| [get_SignTime](./get_signtime/)() const | Obtient le moment où le document a été signé. |
| [get_SubjectName](./get_subjectname/)() | Renvoie le nom distinctif du sujet du certificat qui a été utilisé pour signer le document. |
| [get_VerticalResolution](./get_verticalresolution/)() | Obtient la résolution verticale pour la signature numérique. |
| [get_WindowsVersion](./get_windowsversion/)() | Obtient la version Windows pour la signature numérique. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [ToString](./tostring/)() const override | Renvoie une chaîne conviviale qui affiche la valeur de cet objet. |
| static [Type](./type/)() |  |

## Exemples



Montre comment valider et afficher les informations sur chaque signature dans un document.
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

## Voir aussi

* Namespace [Aspose::Words::DigitalSignatures](../)
* Library [Aspose.Words for C++](../../)
