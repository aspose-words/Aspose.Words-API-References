---
title: "Aspose::Words::DigitalSignatures::DigitalSignatureUtil::LoadSignatures method"
linktitle: "LoadSignatures"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::DigitalSignatures::DigitalSignatureUtil::LoadSignatures method. Carica le firme digitali dal documento usando lo stream in C++."
type: docs
weight: 1000
url: /it/cpp/aspose.words.digitalsignatures/digitalsignatureutil/loadsignatures/
---
## DigitalSignatureUtil::LoadSignatures(const System::SharedPtr\<System::IO::Stream\>\&) method


Carica le firme digitali dal documento usando lo stream.

```cpp
static System::SharedPtr<Aspose::Words::DigitalSignatures::DigitalSignatureCollection> Aspose::Words::DigitalSignatures::DigitalSignatureUtil::LoadSignatures(const System::SharedPtr<System::IO::Stream> &stream)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| flusso | const System::SharedPtr\<System::IO::Stream\>\& | Stream contenente il documento. |

### ReturnValue

Collezione di firme digitali. Restituisce una collezione vuota se il file non è firmato.

## Esempi



Mostra come caricare le firme da un documento firmato digitalmente.
```cpp
// Esistono due modi per caricare la raccolta di firme digitali di un documento firmato utilizzando la classe DigitalSignatureUtil.
// 1 -  Carica da un documento dal file system locale tramite nome file:
System::SharedPtr<Aspose::Words::DigitalSignatures::DigitalSignatureCollection> digitalSignatures = Aspose::Words::DigitalSignatures::DigitalSignatureUtil::LoadSignatures(get_MyDir() + u"Digitally signed.docx");

// Se questa raccolta non è vuota, possiamo verificare che il documento sia firmato digitalmente.
ASSERT_EQ(1, digitalSignatures->get_Count());

// 2 -  Carica da un documento da un FileStream:
{
    System::SharedPtr<System::IO::Stream> stream = System::MakeObject<System::IO::FileStream>(get_MyDir() + u"Digitally signed.docx", System::IO::FileMode::Open);
    digitalSignatures = Aspose::Words::DigitalSignatures::DigitalSignatureUtil::LoadSignatures(stream);
    ASSERT_EQ(1, digitalSignatures->get_Count());
}
```

## Vedi anche

* Class [DigitalSignatureCollection](../../digitalsignaturecollection/)
* Class [DigitalSignatureUtil](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
## DigitalSignatureUtil::LoadSignatures(const System::String\&) method


Carica le firme digitali dal documento.

```cpp
static System::SharedPtr<Aspose::Words::DigitalSignatures::DigitalSignatureCollection> Aspose::Words::DigitalSignatures::DigitalSignatureUtil::LoadSignatures(const System::String &fileName)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| nomeFile | const System::String\& | Percorso del documento. |

### ReturnValue

Collezione di firme digitali. Restituisce una collezione vuota se il file non è firmato.

## Esempi



Mostra come caricare le firme da un documento firmato digitalmente.
```cpp
// Esistono due modi per caricare la raccolta di firme digitali di un documento firmato utilizzando la classe DigitalSignatureUtil.
// 1 -  Carica da un documento dal file system locale tramite nome file:
System::SharedPtr<Aspose::Words::DigitalSignatures::DigitalSignatureCollection> digitalSignatures = Aspose::Words::DigitalSignatures::DigitalSignatureUtil::LoadSignatures(get_MyDir() + u"Digitally signed.docx");

// Se questa raccolta non è vuota, possiamo verificare che il documento sia firmato digitalmente.
ASSERT_EQ(1, digitalSignatures->get_Count());

// 2 -  Carica da un documento da un FileStream:
{
    System::SharedPtr<System::IO::Stream> stream = System::MakeObject<System::IO::FileStream>(get_MyDir() + u"Digitally signed.docx", System::IO::FileMode::Open);
    digitalSignatures = Aspose::Words::DigitalSignatures::DigitalSignatureUtil::LoadSignatures(stream);
    ASSERT_EQ(1, digitalSignatures->get_Count());
}
```


Mostra come rimuovere le firme digitali da un documento firmato digitalmente.
```cpp
// Esistono due modi per utilizzare la classe DigitalSignatureUtil per rimuovere le firme digitali
// da un documento firmato salvando una copia non firmata altrove nel file system locale.
// 1 - Determina le posizioni sia del documento firmato sia della copia non firmata tramite stringhe di nome file:
Aspose::Words::DigitalSignatures::DigitalSignatureUtil::RemoveAllSignatures(get_MyDir() + u"Digitally signed.docx", get_ArtifactsDir() + u"DigitalSignatureUtil.LoadAndRemove.FromString.docx");

// 2 - Determina le posizioni sia del documento firmato sia della copia non firmata tramite stream di file:
{
    System::SharedPtr<System::IO::Stream> streamIn = System::MakeObject<System::IO::FileStream>(get_MyDir() + u"Digitally signed.docx", System::IO::FileMode::Open);
    {
        System::SharedPtr<System::IO::Stream> streamOut = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + u"DigitalSignatureUtil.LoadAndRemove.FromStream.docx", System::IO::FileMode::Create);
        Aspose::Words::DigitalSignatures::DigitalSignatureUtil::RemoveAllSignatures(streamIn, streamOut);
    }
}

// Verifica che entrambi i nostri documenti di output non abbiano firme digitali.
ASSERT_EQ(0, Aspose::Words::DigitalSignatures::DigitalSignatureUtil::LoadSignatures(get_ArtifactsDir() + u"DigitalSignatureUtil.LoadAndRemove.FromString.docx")->get_Count());
ASSERT_EQ(0, Aspose::Words::DigitalSignatures::DigitalSignatureUtil::LoadSignatures(get_ArtifactsDir() + u"DigitalSignatureUtil.LoadAndRemove.FromStream.docx")->get_Count());
```

## Vedi anche

* Class [DigitalSignatureCollection](../../digitalsignaturecollection/)
* Class [DigitalSignatureUtil](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
## DigitalSignatureUtil::LoadSignatures(std::basic_istream\<CharType, Traits\>\&) method




```cpp
template<typename CharType,typename Traits> static System::SharedPtr<Aspose::Words::DigitalSignatures::DigitalSignatureCollection> Aspose::Words::DigitalSignatures::DigitalSignatureUtil::LoadSignatures(std::basic_istream<CharType, Traits> &stream)
```

## Vedi anche

* Class [DigitalSignatureCollection](../../digitalsignaturecollection/)
* Class [DigitalSignatureUtil](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
