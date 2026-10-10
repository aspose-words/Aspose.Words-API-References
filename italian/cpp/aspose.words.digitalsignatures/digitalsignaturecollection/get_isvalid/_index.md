---
title: "Metodo Aspose::Words::DigitalSignatures::DigitalSignatureCollection::get_IsValid"
linktitle: "get_IsValid"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::DigitalSignatures::DigitalSignatureCollection::get_IsValid. Restituisce true se tutte le firme digitali in questa collezione sono valide e il documento non è stato manomesso. Restituisce anche true se non ci sono firme digitali. Restituisce false se almeno una firma digitale è invalida in C++."
type: docs
weight: 8000
url: /it/cpp/aspose.words.digitalsignatures/digitalsignaturecollection/get_isvalid/
---
## DigitalSignatureCollection::get_IsValid method


Restituisce **true** se tutte le firme digitali in questa collezione sono valide e il documento non è stato manomesso. Restituisce anche **true** se non ci sono firme digitali. Restituisce **false** se almeno una firma digitale è invalida.

```cpp
bool Aspose::Words::DigitalSignatures::DigitalSignatureCollection::get_IsValid()
```


## Esempi



Mostra come firmare documenti con certificati X.509.
```cpp
// Verifica che un documento non sia firmato.
ASSERT_FALSE(Aspose::Words::FileFormatUtil::DetectFileFormat(get_MyDir() + u"Document.docx")->get_HasDigitalSignature());

// Crea un oggetto CertificateHolder da un file PKCS12, che utilizzeremo per firmare il documento.
System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certificateHolder = Aspose::Words::DigitalSignatures::CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw", nullptr);

// Ci sono due modi per salvare una copia firmata di un documento sul file system locale:
// 1 - Designare un documento tramite un nome file locale di sistema e salvare una copia firmata in una posizione specificata da un altro nome file.
auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_SignTime(System::DateTime::get_Now());
Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(get_MyDir() + u"Document.docx", get_ArtifactsDir() + u"Document.DigitalSignature.docx", certificateHolder, signOptions);

ASSERT_TRUE(Aspose::Words::FileFormatUtil::DetectFileFormat(get_ArtifactsDir() + u"Document.DigitalSignature.docx")->get_HasDigitalSignature());

// 2 - Prendere un documento da uno stream e salvare una copia firmata in un altro stream.
{
    auto inDoc = System::MakeObject<System::IO::FileStream>(get_MyDir() + u"Document.docx", System::IO::FileMode::Open);
    {
        auto outDoc = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + u"Document.DigitalSignature.docx", System::IO::FileMode::Create);
        Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(inDoc, outDoc, certificateHolder);
    }
}

ASSERT_TRUE(Aspose::Words::FileFormatUtil::DetectFileFormat(get_ArtifactsDir() + u"Document.DigitalSignature.docx")->get_HasDigitalSignature());

// Per favore verifica che tutte le firme digitali del documento siano valide e controlla i loro dettagli.
auto signedDoc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Document.DigitalSignature.docx");
System::SharedPtr<Aspose::Words::DigitalSignatures::DigitalSignatureCollection> digitalSignatureCollection = signedDoc->get_DigitalSignatures();

ASSERT_TRUE(digitalSignatureCollection->get_IsValid());
ASSERT_EQ(1, digitalSignatureCollection->get_Count());
ASSERT_EQ(Aspose::Words::DigitalSignatures::DigitalSignatureType::XmlDsig, digitalSignatureCollection->idx_get(0)->get_SignatureType());
ASSERT_EQ(u"CN=Morzal.Me", signedDoc->get_DigitalSignatures()->idx_get(0)->get_IssuerName());
ASSERT_EQ(u"CN=Morzal.Me", signedDoc->get_DigitalSignatures()->idx_get(0)->get_SubjectName());
```

## Vedi anche

* Class [DigitalSignatureCollection](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
