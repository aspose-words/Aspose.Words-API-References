---
title: "Aspose::Words::FileFormatUtil::DetectFileFormat méthode"
linktitle: "DetectFileFormat"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::FileFormatUtil::DetectFileFormat méthode. Détecte et renvoie les informations sur le format d'un document stocké dans un flux en C++."
type: docs
weight: 3000
url: /fr/cpp/aspose.words/fileformatutil/detectfileformat/
---
## FileFormatUtil::DetectFileFormat(const System::SharedPtr\<System::IO::Stream\>\&) method


Détecte et renvoie les informations sur le format d’un document stocké dans un flux.

```cpp
static System::SharedPtr<Aspose::Words::FileFormatInfo> Aspose::Words::FileFormatUtil::DetectFileFormat(const System::SharedPtr<System::IO::Stream> &stream)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| flux | const System::SharedPtr\<System::IO::Stream\>\& | Le flux. |

### ReturnValue

Un objet [FileFormatInfo](../../fileformatinfo/) qui contient les informations détectées.
## Remarques


Le flux doit être positionné au début du document.

Lorsque cette méthode retourne, la position dans le flux est restaurée à la position d'origine.

Même si cette méthode détecte le format du document, elle ne garantit pas que le document spécifié soit valide. Cette méthode ne fait que détecter le format du document en lisant des données suffisantes pour la détection. Pour vérifier pleinement qu'un document est valide, vous devez charger le document dans un objet [Document](../../document/).

Cette méthode lève [FileCorruptedException](../../filecorruptedexception/) lorsque le format est reconnu, mais la détection ne peut pas se terminer en raison d'une corruption.

## Exemples



Montre comment utiliser les méthodes [FileFormatUtil](../) pour détecter le format d'un document.
```cpp
// Chargez un document à partir d'un fichier sans extension, puis détectez son format de fichier.
{
    System::SharedPtr<System::IO::FileStream> docStream = System::IO::File::OpenRead(get_MyDir() + u"Word document with missing file extension");
    System::SharedPtr<Aspose::Words::FileFormatInfo> info = Aspose::Words::FileFormatUtil::DetectFileFormat(docStream);
    Aspose::Words::LoadFormat loadFormat = info->get_LoadFormat();

    ASSERT_EQ(Aspose::Words::LoadFormat::Doc, loadFormat);

    // Voici deux méthodes pour convertir un LoadFormat en son SaveFormat correspondant.
    // 1 -  Obtenez la chaîne d'extension de fichier pour le LoadFormat, puis obtenez le SaveFormat correspondant à partir de cette chaîne :
    System::String fileExtension = Aspose::Words::FileFormatUtil::LoadFormatToExtension(loadFormat);
    Aspose::Words::SaveFormat saveFormat = Aspose::Words::FileFormatUtil::ExtensionToSaveFormat(fileExtension);

    // 2 -  Convertissez directement le LoadFormat en son SaveFormat :
    saveFormat = Aspose::Words::FileFormatUtil::LoadFormatToSaveFormat(loadFormat);

    // Chargez un document depuis le flux, puis enregistrez-le avec l'extension détectée automatiquement.
    auto doc = System::MakeObject<Aspose::Words::Document>(docStream);

    ASSERT_EQ(u".doc", Aspose::Words::FileFormatUtil::SaveFormatToExtension(saveFormat));

    doc->Save(get_ArtifactsDir() + u"File.SaveToDetectedFileFormat" + Aspose::Words::FileFormatUtil::SaveFormatToExtension(saveFormat));
}
```

## Voir aussi

* Class [FileFormatInfo](../../fileformatinfo/)
* Class [FileFormatUtil](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## FileFormatUtil::DetectFileFormat(const System::String\&) method


Détecte et renvoie les informations sur le format d’un document stocké dans un fichier disque.

```cpp
static System::SharedPtr<Aspose::Words::FileFormatInfo> Aspose::Words::FileFormatUtil::DetectFileFormat(const System::String &fileName)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| fileName | const System::String\& | Le nom du fichier. |

### ReturnValue

Un objet [FileFormatInfo](../../fileformatinfo/) qui contient les informations détectées.
## Remarques


Même si cette méthode détecte le format du document, elle ne garantit pas que le document spécifié soit valide. Cette méthode ne fait que détecter le format du document en lisant des données suffisantes pour la détection. Pour vérifier pleinement qu'un document est valide, vous devez charger le document dans un objet [Document](../../document/).

Cette méthode lève [FileCorruptedException](../../filecorruptedexception/) lorsque le format est reconnu, mais la détection ne peut pas se terminer en raison d'une corruption.

## Exemples



Montre comment utiliser la classe [FileFormatUtil](../) pour détecter le format du document et le chiffrement.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Configurez un objet SaveOptions pour chiffrer le document
// avec un mot de passe lors de l'enregistrement, puis enregistrez le document.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OdtSaveOptions>(Aspose::Words::SaveFormat::Odt);
saveOptions->set_Password(u"MyPassword");

doc->Save(get_ArtifactsDir() + u"File.DetectDocumentEncryption.odt", saveOptions);

// Vérifiez le type de fichier de notre document ainsi que son état de chiffrement.
System::SharedPtr<Aspose::Words::FileFormatInfo> info = Aspose::Words::FileFormatUtil::DetectFileFormat(get_ArtifactsDir() + u"File.DetectDocumentEncryption.odt");

ASSERT_EQ(u".odt", Aspose::Words::FileFormatUtil::LoadFormatToExtension(info->get_LoadFormat()));
ASSERT_TRUE(info->get_IsEncrypted());
```


Montre comment utiliser la classe [FileFormatUtil](../) pour détecter le format du document et la présence de signatures numériques.
```cpp
// Utilisez une instance de FileFormatInfo pour vérifier qu'un document n'est pas signé numériquement.
System::SharedPtr<Aspose::Words::FileFormatInfo> info = Aspose::Words::FileFormatUtil::DetectFileFormat(get_MyDir() + u"Document.docx");

ASSERT_EQ(u".docx", Aspose::Words::FileFormatUtil::LoadFormatToExtension(info->get_LoadFormat()));
ASSERT_FALSE(info->get_HasDigitalSignature());

System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certificateHolder = Aspose::Words::DigitalSignatures::CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw", nullptr);
auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_SignTime(System::DateTime::get_Now());
Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(get_MyDir() + u"Document.docx", get_ArtifactsDir() + u"File.DetectDigitalSignatures.docx", certificateHolder, signOptions);

// Utilisez une nouvelle FileFormatInstance pour confirmer qu'il est signé.
info = Aspose::Words::FileFormatUtil::DetectFileFormat(get_ArtifactsDir() + u"File.DetectDigitalSignatures.docx");

ASSERT_TRUE(info->get_HasDigitalSignature());

// Nous pouvons charger et accéder aux signatures d'un document signé dans une collection comme celle-ci.
ASSERT_EQ(1, Aspose::Words::DigitalSignatures::DigitalSignatureUtil::LoadSignatures(get_ArtifactsDir() + u"File.DetectDigitalSignatures.docx")->get_Count());
```

## Voir aussi

* Class [FileFormatInfo](../../fileformatinfo/)
* Class [FileFormatUtil](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## FileFormatUtil::DetectFileFormat(std::basic_istream\<CharType, Traits\>\&) method




```cpp
template<typename CharType,typename Traits> static System::SharedPtr<Aspose::Words::FileFormatInfo> Aspose::Words::FileFormatUtil::DetectFileFormat(std::basic_istream<CharType, Traits> &stream)
```

## Voir aussi

* Class [FileFormatInfo](../../fileformatinfo/)
* Class [FileFormatUtil](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
