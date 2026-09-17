---
title: "Classe Aspose::Words::Saving::PdfDigitalSignatureDetails"
linktitle: "PdfDigitalSignatureDetails"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Classe Aspose::Words::Saving::PdfDigitalSignatureDetails. Contient les détails pour signer un document PDF avec une signature numérique en C++."
type: docs
weight: 22000
url: /fr/cpp/aspose.words.saving/pdfdigitalsignaturedetails/
---
## PdfDigitalSignatureDetails class


Contient les détails pour signer un document PDF avec une signature numérique.

```cpp
class PdfDigitalSignatureDetails : public System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [get_CertificateHolder](./get_certificateholder/)() const | Renvoie l'objet détenteur du certificat qui contient le certificat utilisé pour signer le document. |
| [get_HashAlgorithm](./get_hashalgorithm/)() const | Obtient l'algorithme de hachage. |
| [get_Location](./get_location/)() const | Obtient l'emplacement de la signature. |
| [get_Reason](./get_reason/)() const | Obtient la raison de la signature. |
| [get_SignatureDate](./get_signaturedate/)() const | Obtient ou définit la date de la signature. |
| [get_TimestampSettings](./get_timestampsettings/)() const | Obtient ou définit les paramètres de l'horodatage de la signature numérique. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [PdfDigitalSignatureDetails](./pdfdigitalsignaturedetails/)() | Initialise une instance de cette classe. |
| [PdfDigitalSignatureDetails](./pdfdigitalsignaturedetails/)(const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\&, const System::String\&, const System::String\&, System::DateTime) | Initialise une instance de cette classe. |
| [set_CertificateHolder](./set_certificateholder/)(const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\&) | Renvoie l'objet détenteur du certificat qui contient le certificat utilisé pour signer le document. |
| [set_HashAlgorithm](./set_hashalgorithm/)(Aspose::Words::Saving::PdfDigitalSignatureHashAlgorithm) | Définit l'algorithme de hachage. |
| [set_Location](./set_location/)(const System::String\&) | Définit l'emplacement de la signature. |
| [set_Reason](./set_reason/)(const System::String\&) | Définit la raison de la signature. |
| [set_SignatureDate](./set_signaturedate/)(System::DateTime) | Définisseur pour [Aspose::Words::Saving::PdfDigitalSignatureDetails::get_SignatureDate](./get_signaturedate/). |
| [set_TimestampSettings](./set_timestampsettings/)(const System::SharedPtr\<Aspose::Words::Saving::PdfDigitalSignatureTimestampSettings\>\&) | Définisseur pour [Aspose::Words::Saving::PdfDigitalSignatureDetails::get_TimestampSettings](./get_timestampsettings/). |
| static [Type](./type/)() |  |
## Remarques


Pour le moment, la signature numérique de documents PDF n'est disponible que sur .NET 3.5 ou supérieur.

Pour signer numériquement un document PDF lorsqu'il est créé par Aspose.Words, définissez la propriété [DigitalSignatureDetails](../pdfsaveoptions/get_digitalsignaturedetails/) sur un objet [PdfDigitalSignatureDetails](./) valide, puis enregistrez le document au format PDF en passant les [PdfSaveOptions](../pdfsaveoptions/) comme paramètre à la méthode [Save()](../).

Aspose.Words crée une signature PKCS#7 sur l'ensemble du document PDF et utilise le filtre "Adobe.PPKMS" ainsi que le sous-filtre "adbe.pkcs7.sha1" lors de la création d'une signature numérique.

## Voir aussi

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
