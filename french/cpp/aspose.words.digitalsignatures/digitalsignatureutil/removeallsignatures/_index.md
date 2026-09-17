---
title: "Aspose::Words::DigitalSignatures::DigitalSignatureUtil::RemoveAllSignatures méthode"
linktitle: "RemoveAllSignatures"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::DigitalSignatures::DigitalSignatureUtil::RemoveAllSignatures méthode. Supprime toutes les signatures numériques du document dans le flux source et écrit le document non signé dans le flux de destination. La sortie sera écrite au début du flux et la taille du flux sera mise à jour avec la longueur du contenu. Les formats suivants sont compatibles pour la suppression de signatures numériques : Doc, Dot, Docx, Dotx, Docm, Dotm, Odt, Ott en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words.digitalsignatures/digitalsignatureutil/removeallsignatures/
---
## DigitalSignatureUtil::RemoveAllSignatures(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&) method


Supprime toutes les signatures numériques du document dans le flux source et écrit le document non signé dans le flux de destination. **La sortie sera écrite au début du flux et la taille du flux sera mise à jour avec la longueur du contenu.**Les formats suivants sont compatibles pour la suppression de signatures numériques : [Doc](../../../aspose.words/loadformat/), [Dot](../../../aspose.words/loadformat/), [Docx](../../../aspose.words/loadformat/), [Dotx](../../../aspose.words/loadformat/), [Docm](../../../aspose.words/loadformat/), [Dotm](../../../aspose.words/loadformat/), [Odt](../../../aspose.words/loadformat/), [Ott](../../../aspose.words/loadformat/).

```cpp
static void Aspose::Words::DigitalSignatures::DigitalSignatureUtil::RemoveAllSignatures(const System::SharedPtr<System::IO::Stream> &srcStream, const System::SharedPtr<System::IO::Stream> &dstStream)
```


## Exemples



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

* Class [DigitalSignatureUtil](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
## DigitalSignatureUtil::RemoveAllSignatures(const System::String\&, const System::String\&) method


Supprime toutes les signatures numériques du fichier source et écrit le fichier non signé dans le fichier de destination. Les formats suivants sont compatibles pour la suppression de signatures numériques : [Doc](../../../aspose.words/loadformat/), [Dot](../../../aspose.words/loadformat/), [Docx](../../../aspose.words/loadformat/), [Dotx](../../../aspose.words/loadformat/), [Docm](../../../aspose.words/loadformat/), [Dotm](../../../aspose.words/loadformat/), [Odt](../../../aspose.words/loadformat/), [Ott](../../../aspose.words/loadformat/).

```cpp
static void Aspose::Words::DigitalSignatures::DigitalSignatureUtil::RemoveAllSignatures(const System::String &srcFileName, const System::String &dstFileName)
```


## Exemples



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

* Class [DigitalSignatureUtil](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
## DigitalSignatureUtil::RemoveAllSignatures(std::basic_istream\<CharType, Traits\>\&, std::basic_ostream\<CharType, Traits\>\&) method




```cpp
template<typename CharType,typename Traits> static void Aspose::Words::DigitalSignatures::DigitalSignatureUtil::RemoveAllSignatures(std::basic_istream<CharType, Traits> &srcStream, std::basic_ostream<CharType, Traits> &dstStream)
```

## Voir aussi

* Class [DigitalSignatureUtil](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
