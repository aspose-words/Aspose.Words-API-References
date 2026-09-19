---
title: "Aspose::Words::FileFormatInfo classe"
linktitle: "FileFormatInfo"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::FileFormatInfo classe. Contiene i dati restituiti dai metodi di rilevamento del formato documento di FileFormatUtil. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 27000
url: /it/cpp/aspose.words/fileformatinfo/
---
## FileFormatInfo class


Contiene i dati restituiti dai metodi di rilevamento del formato documento di [FileFormatUtil](../fileformatutil/). Per saperne di più, visita l'articolo di documentazione [Detect File Format and Check Format Compatibility](https://docs.aspose.com/words/cpp/detect-file-format-and-check-format-compatibility/).

```cpp
class FileFormatInfo : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get_Encoding](./get_encoding/)() const | Ottiene la codifica rilevata, se applicabile al formato del documento corrente. Al momento rileva la codifica solo per i documenti HTML. |
| [get_HasDigitalSignature](./get_hasdigitalsignature/)() const | Restituisce **true** se questo documento contiene una firma digitale. Questa proprietà indica semplicemente che una firma digitale è presente su un documento, ma non specifica se la firma è valida o meno. |
| [get_HasMacros](./get_hasmacros/)() const | Restituisce **true** se questo documento contiene macro VBA. |
| [get_IsEncrypted](./get_isencrypted/)() const | Restituisce **true** se il documento è crittografato e richiede una password per l'apertura. |
| [get_LoadFormat](./get_loadformat/)() const | Ottiene il formato del documento rilevato. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Note


Non si creano istanze di questa classe direttamente. Gli oggetti di questa classe sono restituiti dai metodi [DetectFileFormat()](../).

## Esempi



Mostra come utilizzare la classe [FileFormatUtil](../fileformatutil/) per rilevare il formato del documento e la crittografia.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Configura un oggetto SaveOptions per crittografare il documento
// con una password quando lo salviamo, e poi salva il documento.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OdtSaveOptions>(Aspose::Words::SaveFormat::Odt);
saveOptions->set_Password(u"MyPassword");

doc->Save(get_ArtifactsDir() + u"File.DetectDocumentEncryption.odt", saveOptions);

// Verifica il tipo di file del nostro documento e il suo stato di crittografia.
System::SharedPtr<Aspose::Words::FileFormatInfo> info = Aspose::Words::FileFormatUtil::DetectFileFormat(get_ArtifactsDir() + u"File.DetectDocumentEncryption.odt");

ASSERT_EQ(u".odt", Aspose::Words::FileFormatUtil::LoadFormatToExtension(info->get_LoadFormat()));
ASSERT_TRUE(info->get_IsEncrypted());
```


Mostra come utilizzare la classe [FileFormatUtil](../fileformatutil/) per rilevare il formato del documento e la presenza di firme digitali.
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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
