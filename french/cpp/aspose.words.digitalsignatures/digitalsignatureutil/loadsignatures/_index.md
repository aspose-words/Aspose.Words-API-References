---
title: "Aspose::Words::DigitalSignatures::DigitalSignatureUtil::LoadSignatures method"
linktitle: "LoadSignatures"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::DigitalSignatures::DigitalSignatureUtil::LoadSignatures method. Charge les signatures numériques depuis le document en utilisant un flux en C++."
type: docs
weight: 1000
url: /fr/cpp/aspose.words.digitalsignatures/digitalsignatureutil/loadsignatures/
---
## DigitalSignatureUtil::LoadSignatures(const System::SharedPtr\<System::IO::Stream\>\&) method


Charge les signatures numériques depuis le document en utilisant un flux.

```cpp
static System::SharedPtr<Aspose::Words::DigitalSignatures::DigitalSignatureCollection> Aspose::Words::DigitalSignatures::DigitalSignatureUtil::LoadSignatures(const System::SharedPtr<System::IO::Stream> &stream)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| flux | const System::SharedPtr\<System::IO::Stream\>\& | Flux contenant le document. |

### ReturnValue

Collection de signatures numériques. Retourne une collection vide si le fichier n'est pas signé.

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

## Voir aussi

* Class [DigitalSignatureCollection](../../digitalsignaturecollection/)
* Class [DigitalSignatureUtil](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
## DigitalSignatureUtil::LoadSignatures(const System::String\&) method


Charge les signatures numériques depuis le document.

```cpp
static System::SharedPtr<Aspose::Words::DigitalSignatures::DigitalSignatureCollection> Aspose::Words::DigitalSignatures::DigitalSignatureUtil::LoadSignatures(const System::String &fileName)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| fileName | const System::String\& | Chemin vers le document. |

### ReturnValue

Collection de signatures numériques. Retourne une collection vide si le fichier n'est pas signé.

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

* Class [DigitalSignatureCollection](../../digitalsignaturecollection/)
* Class [DigitalSignatureUtil](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
## DigitalSignatureUtil::LoadSignatures(std::basic_istream\<CharType, Traits\>\&) method




```cpp
template<typename CharType,typename Traits> static System::SharedPtr<Aspose::Words::DigitalSignatures::DigitalSignatureCollection> Aspose::Words::DigitalSignatures::DigitalSignatureUtil::LoadSignatures(std::basic_istream<CharType, Traits> &stream)
```

## Voir aussi

* Class [DigitalSignatureCollection](../../digitalsignaturecollection/)
* Class [DigitalSignatureUtil](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
