---
title: "Metodo Aspose::Words::FileFormatInfo::get_HasDigitalSignature"
linktitle: "get_HasDigitalSignature"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::FileFormatInfo::get_HasDigitalSignature. Restituisce true se questo documento contiene una firma digitale. Questa proprietà indica semplicemente che una firma digitale è presente su un documento, ma non specifica se la firma è valida o meno in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words/fileformatinfo/get_hasdigitalsignature/
---
## FileFormatInfo::get_HasDigitalSignature method


Restituisce **true** se questo documento contiene una firma digitale. Questa proprietà indica semplicemente che una firma digitale è presente su un documento, ma non specifica se la firma è valida o meno.

```cpp
bool Aspose::Words::FileFormatInfo::get_HasDigitalSignature() const
```

## Note


Questa proprietà esiste per aiutarti a distinguere i documenti firmati digitalmente da quelli non firmati. Se utilizzi Aspose.Words per modificare e salvare un documento firmato digitalmente, la firma digitale verrà persa. Questo è previsto, poiché una firma digitale serve a garantire l'autenticità di un documento. Utilizzando questa proprietà puoi rilevare i documenti firmati digitalmente prima di elaborarli allo stesso modo dei documenti normali e intraprendere un'azione per evitare la perdita della firma digitale, ad esempio notificare l'utente.

## Esempi



Mostra come utilizzare la classe [FileFormatUtil](../../fileformatutil/) per rilevare il formato del documento e la presenza di firme digitali.
```cpp
// Utilizza un'istanza di FileFormatInfo per verificare che un documento non sia firmato digitalmente.
System::SharedPtr<Aspose::Words::FileFormatInfo> info = Aspose::Words::FileFormatUtil::DetectFileFormat(get_MyDir() + u"Document.docx");

ASSERT_EQ(u".docx", Aspose::Words::FileFormatUtil::LoadFormatToExtension(info->get_LoadFormat()));
ASSERT_FALSE(info->get_HasDigitalSignature());

System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certificateHolder = Aspose::Words::DigitalSignatures::CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw", nullptr);
auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_SignTime(System::DateTime::get_Now());
Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(get_MyDir() + u"Document.docx", get_ArtifactsDir() + u"File.DetectDigitalSignatures.docx", certificateHolder, signOptions);

// Utilizza una nuova FileFormatInstance per confermare che sia firmato.
info = Aspose::Words::FileFormatUtil::DetectFileFormat(get_ArtifactsDir() + u"File.DetectDigitalSignatures.docx");

ASSERT_TRUE(info->get_HasDigitalSignature());

// Possiamo caricare e accedere alle firme di un documento firmato in una collezione come questa.
ASSERT_EQ(1, Aspose::Words::DigitalSignatures::DigitalSignatureUtil::LoadSignatures(get_ArtifactsDir() + u"File.DetectDigitalSignatures.docx")->get_Count());
```

## Vedi anche

* Class [FileFormatInfo](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
