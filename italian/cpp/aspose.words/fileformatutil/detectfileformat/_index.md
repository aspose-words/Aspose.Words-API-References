---
title: "Aspose::Words::FileFormatUtil::DetectFileFormat method"
linktitle: "DetectFileFormat"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::FileFormatUtil::DetectFileFormat method. Rileva e restituisce le informazioni sul formato di un documento memorizzato in uno stream in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words/fileformatutil/detectfileformat/
---
## FileFormatUtil::DetectFileFormat(const System::SharedPtr\<System::IO::Stream\>\&) method


Rileva e restituisce le informazioni su un formato di un documento memorizzato in uno stream.

```cpp
static System::SharedPtr<Aspose::Words::FileFormatInfo> Aspose::Words::FileFormatUtil::DetectFileFormat(const System::SharedPtr<System::IO::Stream> &stream)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| flusso | const System::SharedPtr\<System::IO::Stream\>\& | Lo stream. |

### ReturnValue

Un oggetto [FileFormatInfo](../../fileformatinfo/) che contiene le informazioni rilevate.
## Note


Lo stream deve essere posizionato all'inizio del documento.

Quando questo metodo termina, la posizione nello stream viene ripristinata alla posizione originale.

Anche se questo metodo rileva il formato del documento, non garantisce che il documento specificato sia valido. Questo metodo rileva il formato del documento solo leggendo dati sufficienti per il rilevamento. Per verificare completamente che un documento sia valido è necessario caricare il documento in un oggetto [Document](../../document/).

Questo metodo genera [FileCorruptedException](../../filecorruptedexception/) quando il formato è riconosciuto, ma il rilevamento non può completarsi a causa della corruzione.

## Esempi



Mostra come utilizzare i metodi [FileFormatUtil](../) per rilevare il formato di un documento.
```cpp
// Carica un documento da un file a cui manca l'estensione e quindi rileva il suo formato file.
{
    System::SharedPtr<System::IO::FileStream> docStream = System::IO::File::OpenRead(get_MyDir() + u"Word document with missing file extension");
    System::SharedPtr<Aspose::Words::FileFormatInfo> info = Aspose::Words::FileFormatUtil::DetectFileFormat(docStream);
    Aspose::Words::LoadFormat loadFormat = info->get_LoadFormat();

    ASSERT_EQ(Aspose::Words::LoadFormat::Doc, loadFormat);

    // Di seguito sono riportati due metodi per convertire un LoadFormat nel relativo SaveFormat.
    // 1 -  Ottieni la stringa dell'estensione file per il LoadFormat, quindi ottieni il SaveFormat corrispondente da quella stringa:
    System::String fileExtension = Aspose::Words::FileFormatUtil::LoadFormatToExtension(loadFormat);
    Aspose::Words::SaveFormat saveFormat = Aspose::Words::FileFormatUtil::ExtensionToSaveFormat(fileExtension);

    // 2 -  Converti direttamente il LoadFormat nel suo SaveFormat:
    saveFormat = Aspose::Words::FileFormatUtil::LoadFormatToSaveFormat(loadFormat);

    // Carica un documento dallo stream e poi salvalo con l'estensione file rilevata automaticamente.
    auto doc = System::MakeObject<Aspose::Words::Document>(docStream);

    ASSERT_EQ(u".doc", Aspose::Words::FileFormatUtil::SaveFormatToExtension(saveFormat));

    doc->Save(get_ArtifactsDir() + u"File.SaveToDetectedFileFormat" + Aspose::Words::FileFormatUtil::SaveFormatToExtension(saveFormat));
}
```

## Vedi anche

* Class [FileFormatInfo](../../fileformatinfo/)
* Class [FileFormatUtil](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## FileFormatUtil::DetectFileFormat(const System::String\&) method


Rileva e restituisce le informazioni su un formato di un documento memorizzato in un file su disco.

```cpp
static System::SharedPtr<Aspose::Words::FileFormatInfo> Aspose::Words::FileFormatUtil::DetectFileFormat(const System::String &fileName)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| nomeFile | const System::String\& | Il nome del file. |

### ReturnValue

Un oggetto [FileFormatInfo](../../fileformatinfo/) che contiene le informazioni rilevate.
## Note


Anche se questo metodo rileva il formato del documento, non garantisce che il documento specificato sia valido. Questo metodo rileva il formato del documento solo leggendo dati sufficienti per il rilevamento. Per verificare completamente che un documento sia valido è necessario caricare il documento in un oggetto [Document](../../document/).

Questo metodo genera [FileCorruptedException](../../filecorruptedexception/) quando il formato è riconosciuto, ma il rilevamento non può completarsi a causa della corruzione.

## Esempi



Mostra come utilizzare la classe [FileFormatUtil](../) per rilevare il formato del documento e la crittografia.
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


Mostra come utilizzare la classe [FileFormatUtil](../) per rilevare il formato del documento e la presenza di firme digitali.
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

* Class [FileFormatInfo](../../fileformatinfo/)
* Class [FileFormatUtil](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## FileFormatUtil::DetectFileFormat(std::basic_istream\<CharType, Traits\>\&) method




```cpp
template<typename CharType,typename Traits> static System::SharedPtr<Aspose::Words::FileFormatInfo> Aspose::Words::FileFormatUtil::DetectFileFormat(std::basic_istream<CharType, Traits> &stream)
```

## Vedi anche

* Class [FileFormatInfo](../../fileformatinfo/)
* Class [FileFormatUtil](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
