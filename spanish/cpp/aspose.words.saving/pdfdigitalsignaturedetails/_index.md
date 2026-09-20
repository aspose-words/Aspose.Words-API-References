---
title: "Clase Aspose::Words::Saving::PdfDigitalSignatureDetails"
linktitle: "PdfDigitalSignatureDetails"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Clase Aspose::Words::Saving::PdfDigitalSignatureDetails. Contiene detalles para firmar un documento PDF con una firma digital en C++."
type: docs
weight: 22000
url: /es/cpp/aspose.words.saving/pdfdigitalsignaturedetails/
---
## PdfDigitalSignatureDetails class


Contiene detalles para firmar un documento PDF con una firma digital.

```cpp
class PdfDigitalSignatureDetails : public System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [get_CertificateHolder](./get_certificateholder/)() const | Devuelve el objeto titular del certificado que contiene el certificado utilizado para firmar el documento. |
| [get_HashAlgorithm](./get_hashalgorithm/)() const | Obtiene el algoritmo de hash. |
| [get_Location](./get_location/)() const | Obtiene la ubicación de la firma. |
| [get_Reason](./get_reason/)() const | Obtiene la razón de la firma. |
| [get_SignatureDate](./get_signaturedate/)() const | Obtiene o establece la fecha de la firma. |
| [get_TimestampSettings](./get_timestampsettings/)() const | Obtiene o establece la configuración de la marca de tiempo de la firma digital. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [PdfDigitalSignatureDetails](./pdfdigitalsignaturedetails/)() | Inicializa una instancia de esta clase. |
| [PdfDigitalSignatureDetails](./pdfdigitalsignaturedetails/)(const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\&, const System::String\&, const System::String\&, System::DateTime) | Inicializa una instancia de esta clase. |
| [set_CertificateHolder](./set_certificateholder/)(const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\&) | Devuelve el objeto titular del certificado que contiene el certificado utilizado para firmar el documento. |
| [set_HashAlgorithm](./set_hashalgorithm/)(Aspose::Words::Saving::PdfDigitalSignatureHashAlgorithm) | Establece el algoritmo hash. |
| [set_Location](./set_location/)(const System::String\&) | Establece la ubicación de la firma. |
| [set_Reason](./set_reason/)(const System::String\&) | Establece el motivo de la firma. |
| [set_SignatureDate](./set_signaturedate/)(System::DateTime) | Método establecedor para [Aspose::Words::Saving::PdfDigitalSignatureDetails::get_SignatureDate](./get_signaturedate/). |
| [set_TimestampSettings](./set_timestampsettings/)(const System::SharedPtr\<Aspose::Words::Saving::PdfDigitalSignatureTimestampSettings\>\&) | Método establecedor para [Aspose::Words::Saving::PdfDigitalSignatureDetails::get_TimestampSettings](./get_timestampsettings/). |
| static [Type](./type/)() |  |
## Observaciones


En este momento, la firma digital de documentos PDF solo está disponible en .NET 3.5 o superior.

Para firmar digitalmente un documento PDF cuando es creado por Aspose.Words, establezca la propiedad [DigitalSignatureDetails](../pdfsaveoptions/get_digitalsignaturedetails/) a un objeto válido de [PdfDigitalSignatureDetails](./) y luego guarde el documento en formato PDF pasando [PdfSaveOptions](../pdfsaveoptions/) como parámetro al método [Save()](../).

Aspose.Words crea una firma PKCS#7 sobre todo el documento PDF y utiliza el filtro "Adobe.PPKMS" y el subfiltro "adbe.pkcs7.sha1" al crear una firma digital.

## Ver también

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
