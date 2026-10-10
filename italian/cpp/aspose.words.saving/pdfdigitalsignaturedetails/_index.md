---
title: "Aspose::Words::Saving::PdfDigitalSignatureDetails class"
linktitle: "PdfDigitalSignatureDetails"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::PdfDigitalSignatureDetails class. Contiene i dettagli per firmare un documento PDF con una firma digitale in C++."
type: docs
weight: 22000
url: /it/cpp/aspose.words.saving/pdfdigitalsignaturedetails/
---
## PdfDigitalSignatureDetails class


Contiene i dettagli per firmare un documento PDF con una firma digitale.

```cpp
class PdfDigitalSignatureDetails : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get_CertificateHolder](./get_certificateholder/)() const | Restituisce l'oggetto del titolare del certificato che contiene il certificato utilizzato per firmare il documento. |
| [get_HashAlgorithm](./get_hashalgorithm/)() const | Ottiene l'algoritmo di hash. |
| [get_Location](./get_location/)() const | Ottiene la posizione della firma. |
| [get_Reason](./get_reason/)() const | Ottiene il motivo della firma. |
| [get_SignatureDate](./get_signaturedate/)() const | Ottiene o imposta la data della firma. |
| [get_TimestampSettings](./get_timestampsettings/)() const | Ottiene o imposta le impostazioni del timestamp della firma digitale. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [PdfDigitalSignatureDetails](./pdfdigitalsignaturedetails/)() | Inizializza un'istanza di questa classe. |
| [PdfDigitalSignatureDetails](./pdfdigitalsignaturedetails/)(const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\&, const System::String\&, const System::String\&, System::DateTime) | Inizializza un'istanza di questa classe. |
| [set_CertificateHolder](./set_certificateholder/)(const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\&) | Restituisce l'oggetto del titolare del certificato che contiene il certificato utilizzato per firmare il documento. |
| [set_HashAlgorithm](./set_hashalgorithm/)(Aspose::Words::Saving::PdfDigitalSignatureHashAlgorithm) | Imposta l'algoritmo hash. |
| [set_Location](./set_location/)(const System::String\&) | Imposta la posizione della firma. |
| [set_Reason](./set_reason/)(const System::String\&) | Imposta il motivo della firma. |
| [set_SignatureDate](./set_signaturedate/)(System::DateTime) | Impostatore per [Aspose::Words::Saving::PdfDigitalSignatureDetails::get_SignatureDate](./get_signaturedate/). |
| [set_TimestampSettings](./set_timestampsettings/)(const System::SharedPtr\<Aspose::Words::Saving::PdfDigitalSignatureTimestampSettings\>\&) | Impostatore per [Aspose::Words::Saving::PdfDigitalSignatureDetails::get_TimestampSettings](./get_timestampsettings/). |
| static [Type](./type/)() |  |
## Note


Al momento la firma digitale di documenti PDF è disponibile solo su .NET 3.5 o versioni successive.

Per firmare digitalmente un documento PDF quando viene creato da Aspose.Words, impostare la proprietà [DigitalSignatureDetails](../pdfsaveoptions/get_digitalsignaturedetails/) su un oggetto [PdfDigitalSignatureDetails](./) valido e quindi salvare il documento nel formato PDF passando [PdfSaveOptions](../pdfsaveoptions/) come parametro al metodo [Save()](../).

Aspose.Words crea una firma PKCS#7 sull'intero documento PDF e utilizza il filtro "Adobe.PPKMS" e il sottofiltro "adbe.pkcs7.sha1" durante la creazione di una firma digitale.

## Vedi anche

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
