---
title: "Aspose::Words::DigitalSignatures::SignOptions class"
linktitle: "SignOptions"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::DigitalSignatures::SignOptions classe. Permet de spécifier des options pour la signature de documents. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 5000
url: /fr/cpp/aspose.words.digitalsignatures/signoptions/
---
## SignOptions class


Permet de spécifier des options pour la signature de documents. Pour en savoir plus, consultez l'article de documentation [Work with Digital Signatures](https://docs.aspose.com/words/cpp/working-with-digital-signatures/).

```cpp
class SignOptions : public System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [get_ApplicationVersion](./get_applicationversion/)() const | Obtient ou définit la version de l'application pour la signature numérique. La valeur par défaut est "12.0". |
| [get_ColorDepth](./get_colordepth/)() const | Obtient ou définit la profondeur de couleur pour la signature numérique. La valeur par défaut est 32. |
| [get_Comments](./get_comments/)() const | Spécifie les commentaires sur la signature numérique. La valeur par défaut est **empty string**. |
| [get_DecryptionPassword](./get_decryptionpassword/)() const | Le mot de passe pour déchiffrer le document source. La valeur par défaut est **empty string**. |
| [get_HorizontalResolution](./get_horizontalresolution/)() const | Obtient ou définit la résolution horizontale pour la signature numérique. La valeur par défaut est 1920. |
| [get_OfficeVersion](./get_officeversion/)() const | Obtient ou définit la version d'Office pour la signature numérique. La valeur par défaut est "12.0". |
| [get_ProviderId](./get_providerid/)() const | Spécifie l'ID de classe du fournisseur de signature. La valeur par défaut est **Empty (all zeroes) Guid**. |
| [get_SignatureLineId](./get_signaturelineid/)() const | Identifiant de la ligne de signature. La valeur par défaut est **Empty (all zeroes) Guid**. |
| [get_SignatureLineImage](./get_signaturelineimage/)() const | L'image qui sera affichée dans le [SignatureLine](../../aspose.words.drawing/signatureline/) associé. La valeur par défaut est **null**. |
| [get_SignTime](./get_signtime/)() const | La date de signature. La valeur par défaut est **current time** (**Now**) |
| [get_VerticalResolution](./get_verticalresolution/)() const | Obtient ou définit la résolution verticale pour la signature numérique. La valeur par défaut est 1200. |
| [get_WindowsVersion](./get_windowsversion/)() const | Obtient ou définit la version de Windows pour la signature numérique. La valeur par défaut est "6.1". |
| [get_XmlDsigLevel](./get_xmldsiglevel/)() const | Spécifie le niveau d'une signature numérique basé sur la norme XML-DSig. La valeur par défaut est [XmlDSig](../xmldsiglevel/). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_ApplicationVersion](./set_applicationversion/)(const System::String\&) | Mutateur pour [Aspose::Words::DigitalSignatures::SignOptions::get_ApplicationVersion](./get_applicationversion/). |
| [set_ColorDepth](./set_colordepth/)(int32_t) | Mutateur pour [Aspose::Words::DigitalSignatures::SignOptions::get_ColorDepth](./get_colordepth/). |
| [set_Comments](./set_comments/)(const System::String\&) | Mutateur pour [Aspose::Words::DigitalSignatures::SignOptions::get_Comments](./get_comments/). |
| [set_DecryptionPassword](./set_decryptionpassword/)(const System::String\&) | Mutateur pour [Aspose::Words::DigitalSignatures::SignOptions::get_DecryptionPassword](./get_decryptionpassword/). |
| [set_HorizontalResolution](./set_horizontalresolution/)(int32_t) | Mutateur pour [Aspose::Words::DigitalSignatures::SignOptions::get_HorizontalResolution](./get_horizontalresolution/). |
| [set_OfficeVersion](./set_officeversion/)(const System::String\&) | Mutateur pour [Aspose::Words::DigitalSignatures::SignOptions::get_OfficeVersion](./get_officeversion/). |
| [set_ProviderId](./set_providerid/)(System::Guid) | Mutateur pour [Aspose::Words::DigitalSignatures::SignOptions::get_ProviderId](./get_providerid/). |
| [set_SignatureLineId](./set_signaturelineid/)(System::Guid) | Identifiant de la ligne de signature. La valeur par défaut est **Empty (all zeroes) Guid**. |
| [set_SignatureLineImage](./set_signaturelineimage/)(const System::ArrayPtr\<uint8_t\>\&) | L'image qui sera affichée dans le [SignatureLine](../../aspose.words.drawing/signatureline/) associé. La valeur par défaut est **null**. |
| [set_SignTime](./set_signtime/)(System::DateTime) | Mutateur pour [Aspose::Words::DigitalSignatures::SignOptions::get_SignTime](./get_signtime/). |
| [set_VerticalResolution](./set_verticalresolution/)(int32_t) | Mutateur pour [Aspose::Words::DigitalSignatures::SignOptions::get_VerticalResolution](./get_verticalresolution/). |
| [set_WindowsVersion](./set_windowsversion/)(const System::String\&) | Mutateur pour [Aspose::Words::DigitalSignatures::SignOptions::get_WindowsVersion](./get_windowsversion/). |
| [set_XmlDsigLevel](./set_xmldsiglevel/)(Aspose::Words::DigitalSignatures::XmlDsigLevel) | Définisseur pour [Aspose::Words::DigitalSignatures::SignOptions::get_XmlDsigLevel](./get_xmldsiglevel/). |
| [SignOptions](./signoptions/)() |  |
| static [Type](./type/)() |  |

## Exemples



Montre comment signer numériquement des documents.
```cpp
// Créez un certificat X.509 à partir d'un magasin PKCS#12, qui doit contenir une clé privée.
System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certificateHolder = Aspose::Words::DigitalSignatures::CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw");

// Créez un commentaire et une date qui seront appliqués avec notre nouvelle signature numérique.
auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_Comments(u"My comment");
signOptions->set_SignTime(System::DateTime::get_Now());

// Prenez un document non signé depuis le système de fichiers local via un flux de fichier,
// puis créez une copie signée déterminée par le nom de fichier du flux de sortie.
{
    System::SharedPtr<System::IO::Stream> streamIn = System::MakeObject<System::IO::FileStream>(get_MyDir() + u"Document.docx", System::IO::FileMode::Open);
    {
        System::SharedPtr<System::IO::Stream> streamOut = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + u"DigitalSignatureUtil.SignDocument.docx", System::IO::FileMode::OpenOrCreate);
        Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(streamIn, streamOut, certificateHolder, signOptions);
    }
}
```

## Voir aussi

* Namespace [Aspose::Words::DigitalSignatures](../)
* Library [Aspose.Words for C++](../../)
