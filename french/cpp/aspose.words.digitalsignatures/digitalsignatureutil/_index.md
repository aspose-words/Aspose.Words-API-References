---
title: "Aspose::Words::DigitalSignatures::DigitalSignatureUtil classe"
linktitle: "DigitalSignatureUtil"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::DigitalSignatures::DigitalSignatureUtil classe. Fournit des méthodes pour signer le document. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words.digitalsignatures/digitalsignatureutil/
---
## DigitalSignatureUtil class


Fournit des méthodes pour signer un document. Pour en savoir plus, consultez l’article de documentation [Work with Digital Signatures](https://docs.aspose.com/words/cpp/working-with-digital-signatures/).

```cpp
class DigitalSignatureUtil
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [DigitalSignatureUtil](./digitalsignatureutil/)() |  |
| static [LoadSignatures](./loadsignatures/)(const System::String\&) | Charge les signatures numériques depuis le document. |
| static [LoadSignatures](./loadsignatures/)(const System::SharedPtr\<System::IO::Stream\>\&) | Charge les signatures numériques depuis le document en utilisant un flux. |
| static [LoadSignatures](./loadsignatures/)(std::basic_istream\<CharType, Traits\>\&) |  |
| static [RemoveAllSignatures](./removeallsignatures/)(const System::String\&, const System::String\&) | Supprime toutes les signatures numériques du fichier source et écrit le fichier non signé dans le fichier de destination. Les formats suivants sont compatibles pour la suppression de signatures numériques : [Doc](../../aspose.words/loadformat/), [Dot](../../aspose.words/loadformat/), [Docx](../../aspose.words/loadformat/), [Dotx](../../aspose.words/loadformat/), [Docm](../../aspose.words/loadformat/), [Dotm](../../aspose.words/loadformat/), [Odt](../../aspose.words/loadformat/), [Ott](../../aspose.words/loadformat/). |
| static [RemoveAllSignatures](./removeallsignatures/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&) | Supprime toutes les signatures numériques du document dans le flux source et écrit le document non signé dans le flux de destination. **La sortie sera écrite au début du flux et la taille du flux sera mise à jour avec la longueur du contenu.**Les formats suivants sont compatibles pour la suppression de signatures numériques : [Doc](../../aspose.words/loadformat/), [Dot](../../aspose.words/loadformat/), [Docx](../../aspose.words/loadformat/), [Dotx](../../aspose.words/loadformat/), [Docm](../../aspose.words/loadformat/), [Dotm](../../aspose.words/loadformat/), [Odt](../../aspose.words/loadformat/), [Ott](../../aspose.words/loadformat/). |
| static [RemoveAllSignatures](./removeallsignatures/)(std::basic_istream\<CharType, Traits\>\&, std::basic_ostream\<CharType, Traits\>\&) |  |
| static [Sign](./sign/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\&, const System::SharedPtr\<Aspose::Words::DigitalSignatures::SignOptions\>\&) | Signe le document source en utilisant le [CertificateHolder](../certificateholder/) et le [SignOptions](../signoptions/) avec une signature numérique et écrit le document signé dans le flux de destination. Les formats pris en charge sont : [Doc](../../aspose.words/loadformat/), [Dot](../../aspose.words/loadformat/), [Docx](../../aspose.words/loadformat/), [Dotx](../../aspose.words/loadformat/), [Docm](../../aspose.words/loadformat/), [Dotm](../../aspose.words/loadformat/), [Odt](../../aspose.words/loadformat/), [Ott](../../aspose.words/loadformat/).**La sortie sera écrite au début du flux et la taille du flux sera mise à jour avec la longueur du contenu.** |
| static [Sign](./sign/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\&, const System::SharedPtr\<Aspose::Words::DigitalSignatures::SignOptions\>\&) | Signe le document source en utilisant le [CertificateHolder](../certificateholder/) et le [SignOptions](../signoptions/) avec une signature numérique et écrit le document signé dans le fichier de destination. Les formats pris en charge sont : [Doc](../../aspose.words/loadformat/), [Dot](../../aspose.words/loadformat/), [Docx](../../aspose.words/loadformat/), [Dotx](../../aspose.words/loadformat/), [Docm](../../aspose.words/loadformat/), [Dotm](../../aspose.words/loadformat/), [Odt](../../aspose.words/loadformat/), [Ott](../../aspose.words/loadformat/). |
| static [Sign](./sign/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\&) | Signe le document source en utilisant le [CertificateHolder](../certificateholder/) avec une signature numérique et écrit le document signé dans le flux de destination. Les formats pris en charge sont : [Doc](../../aspose.words/loadformat/), [Dot](../../aspose.words/loadformat/), [Docx](../../aspose.words/loadformat/), [Dotx](../../aspose.words/loadformat/), [Docm](../../aspose.words/loadformat/), [Dotm](../../aspose.words/loadformat/), [Odt](../../aspose.words/loadformat/), [Ott](../../aspose.words/loadformat/).**La sortie sera écrite au début du flux et la taille du flux sera mise à jour avec la longueur du contenu.** |
| static [Sign](./sign/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\&) | Signe le document source en utilisant le [CertificateHolder](../certificateholder/) avec une signature numérique et écrit le document signé dans le fichier de destination. Les formats pris en charge sont : [Doc](../../aspose.words/loadformat/), [Dot](../../aspose.words/loadformat/), [Docx](../../aspose.words/loadformat/), [Dotx](../../aspose.words/loadformat/), [Docm](../../aspose.words/loadformat/), [Dotm](../../aspose.words/loadformat/), [Odt](../../aspose.words/loadformat/), [Ott](../../aspose.words/loadformat/). |
| static [Sign](./sign/)(std::basic_istream\<CharType, Traits\>\&, std::basic_ostream\<CharType, Traits\>\&, System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>, System::SharedPtr\<Aspose::Words::DigitalSignatures::SignOptions\>) |  |
| static [Sign](./sign/)(std::basic_istream\<CharType, Traits\>\&, std::basic_ostream\<CharType, Traits\>\&, System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>) |  |
## Remarques


Étant donné que la signature numérique fonctionne avec le contenu du fichier plutôt qu'avec le modèle d'objet [Document](../../aspose.words/document/) ces méthodes sont placées dans une classe séparée.

Les formats pris en charge sont : [Doc](../../aspose.words/loadformat/), [Dot](../../aspose.words/loadformat/), [Docx](../../aspose.words/loadformat/), [Dotx](../../aspose.words/loadformat/), [Docm](../../aspose.words/loadformat/), [Dotm](../../aspose.words/loadformat/), [Odt](../../aspose.words/loadformat/), [Ott](../../aspose.words/loadformat/).

## Exemples



Montre comment charger les signatures d'un document signé numériquement.
```cpp
// Il existe deux façons de charger la collection de signatures numériques d'un document signé en utilisant la classe DigitalSignatureUtil.
// 1 -  Charger à partir d'un document via le nom de fichier du système de fichiers local:
System::SharedPtr<Aspose::Words::DigitalSignatures::DigitalSignatureCollection> digitalSignatures = Aspose::Words::DigitalSignatures::DigitalSignatureUtil::LoadSignatures(get_MyDir() + u"Digitally signed.docx");

// Si cette collection n'est pas vide, nous pouvons alors vérifier que le document est signé numériquement.
ASSERT_EQ(1, digitalSignatures->get_Count());

// 2 -  Charger à partir d'un document via un FileStream:
{
    System::SharedPtr<System::IO::Stream> stream = System::MakeObject<System::IO::FileStream>(get_MyDir() + u"Digitally signed.docx", System::IO::FileMode::Open);
    digitalSignatures = Aspose::Words::DigitalSignatures::DigitalSignatureUtil::LoadSignatures(stream);
    ASSERT_EQ(1, digitalSignatures->get_Count());
}
```


Montre comment supprimer les signatures numériques d'un document signé numériquement.
```cpp
// Il existe deux façons d'utiliser la classe DigitalSignatureUtil pour supprimer les signatures numériques
// d'un document signé en enregistrant une copie non signée ailleurs dans le système de fichiers local.
// 1 - Déterminer les emplacements du document signé et de la copie non signée à l'aide de chaînes de noms de fichiers:
Aspose::Words::DigitalSignatures::DigitalSignatureUtil::RemoveAllSignatures(get_MyDir() + u"Digitally signed.docx", get_ArtifactsDir() + u"DigitalSignatureUtil.LoadAndRemove.FromString.docx");

// 2 - Déterminer les emplacements du document signé et de la copie non signée à l'aide de flux de fichiers:
{
    System::SharedPtr<System::IO::Stream> streamIn = System::MakeObject<System::IO::FileStream>(get_MyDir() + u"Digitally signed.docx", System::IO::FileMode::Open);
    {
        System::SharedPtr<System::IO::Stream> streamOut = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + u"DigitalSignatureUtil.LoadAndRemove.FromStream.docx", System::IO::FileMode::Create);
        Aspose::Words::DigitalSignatures::DigitalSignatureUtil::RemoveAllSignatures(streamIn, streamOut);
    }
}

// Vérifiez que nos deux documents de sortie ne contiennent aucune signature numérique.
ASSERT_EQ(0, Aspose::Words::DigitalSignatures::DigitalSignatureUtil::LoadSignatures(get_ArtifactsDir() + u"DigitalSignatureUtil.LoadAndRemove.FromString.docx")->get_Count());
ASSERT_EQ(0, Aspose::Words::DigitalSignatures::DigitalSignatureUtil::LoadSignatures(get_ArtifactsDir() + u"DigitalSignatureUtil.LoadAndRemove.FromStream.docx")->get_Count());
```

## Voir aussi

* Namespace [Aspose::Words::DigitalSignatures](../)
* Library [Aspose.Words for C++](../../)
