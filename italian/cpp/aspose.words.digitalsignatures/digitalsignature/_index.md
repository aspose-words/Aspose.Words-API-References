---
title: "Aspose::Words::DigitalSignatures::DigitalSignature class"
linktitle: "DigitalSignature"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::DigitalSignatures::DigitalSignature class. Rappresenta una firma digitale su un documento e il risultato della sua verifica. Per saperne di più, visita l'articolo della documentazione in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words.digitalsignatures/digitalsignature/
---
## DigitalSignature class


Rappresenta una firma digitale su un documento e il risultato della sua verifica. Per saperne di più, visita l'articolo di documentazione [Work with Digital Signatures](https://docs.aspose.com/words/cpp/working-with-digital-signatures/).

```cpp
class DigitalSignature : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get_ApplicationVersion](./get_applicationversion/)() | Ottiene la versione dell'applicazione per la firma digitale. |
| [get_CertificateHolder](./get_certificateholder/)() const | Restituisce l'oggetto del titolare del certificato che contiene il certificato utilizzato per firmare il documento. |
| [get_ColorDepth](./get_colordepth/)() | Ottiene la profondità di colore per la firma digitale. |
| [get_Comments](./get_comments/)() | Ottiene il commento sullo scopo della firma. |
| [get_HorizontalResolution](./get_horizontalresolution/)() | Ottiene la risoluzione orizzontale per la firma digitale. |
| [get_IssuerName](./get_issuername/)() | Restituisce il nome distinto del soggetto del certificato dell'emittente. |
| [get_IsValid](./get_isvalid/)() const | Restituisce **true** se questa firma digitale è valida e il documento non è stato manomesso. |
| [get_OfficeVersion](./get_officeversion/)() | Ottiene la versione di Office per la firma digitale. |
| [get_SignatureType](./get_signaturetype/)() const | Ottiene il tipo della firma digitale. |
| [get_SignatureValue](./get_signaturevalue/)() const | Ottiene un array di byte che rappresenta il valore della firma. |
| [get_SignTime](./get_signtime/)() const | Ottiene l'ora in cui il documento è stato firmato. |
| [get_SubjectName](./get_subjectname/)() | Restituisce il nome distinto del soggetto del certificato che è stato utilizzato per firmare il documento. |
| [get_VerticalResolution](./get_verticalresolution/)() | Ottiene la risoluzione verticale per la firma digitale. |
| [get_WindowsVersion](./get_windowsversion/)() | Ottiene la versione di Windows per la firma digitale. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [ToString](./tostring/)() const override | Restituisce una stringa leggibile dall'utente che visualizza il valore di questo oggetto. |
| static [Type](./type/)() |  |

## Esempi



Mostra come convalidare e visualizzare le informazioni su ogni firma in un documento.
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

## Vedi anche

* Namespace [Aspose::Words::DigitalSignatures](../)
* Library [Aspose.Words for C++](../../)
