---
title: "Aspose::Words::DigitalSignatures::DigitalSignatureUtil::RemoveAllSignatures metodo"
linktitle: "RemoveAllSignatures"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::DigitalSignatures::DigitalSignatureUtil::RemoveAllSignatures metodo. Rimuove tutte le firme digitali dal documento nello stream di origine e scrive il documento non firmato nello stream di destinazione. L'output verrà scritto all'inizio dello stream e la dimensione dello stream verrà aggiornata con la lunghezza del contenuto. I seguenti formati sono compatibili per la rimozione della firma digitale: Doc, Dot, Docx, Dotx, Docm, Dotm, Odt, Ott in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words.digitalsignatures/digitalsignatureutil/removeallsignatures/
---
## DigitalSignatureUtil::RemoveAllSignatures(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&) method


Rimuove tutte le firme digitali dal documento nello stream di origine e scrive il documento non firmato nello stream di destinazione. **L'output verrà scritto all'inizio dello stream e la dimensione dello stream verrà aggiornata con la lunghezza del contenuto.**I seguenti formati sono compatibili per la rimozione della firma digitale: [Doc](../../../aspose.words/loadformat/), [Dot](../../../aspose.words/loadformat/), [Docx](../../../aspose.words/loadformat/), [Dotx](../../../aspose.words/loadformat/), [Docm](../../../aspose.words/loadformat/), [Dotm](../../../aspose.words/loadformat/), [Odt](../../../aspose.words/loadformat/), [Ott](../../../aspose.words/loadformat/).

```cpp
static void Aspose::Words::DigitalSignatures::DigitalSignatureUtil::RemoveAllSignatures(const System::SharedPtr<System::IO::Stream> &srcStream, const System::SharedPtr<System::IO::Stream> &dstStream)
```


## Esempi



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

* Class [DigitalSignatureUtil](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
## DigitalSignatureUtil::RemoveAllSignatures(const System::String\&, const System::String\&) method


Rimuove tutte le firme digitali dal file di origine e scrive il file non firmato nel file di destinazione. I seguenti formati sono compatibili per la rimozione della firma digitale: [Doc](../../../aspose.words/loadformat/), [Dot](../../../aspose.words/loadformat/), [Docx](../../../aspose.words/loadformat/), [Dotx](../../../aspose.words/loadformat/), [Docm](../../../aspose.words/loadformat/), [Dotm](../../../aspose.words/loadformat/), [Odt](../../../aspose.words/loadformat/), [Ott](../../../aspose.words/loadformat/).

```cpp
static void Aspose::Words::DigitalSignatures::DigitalSignatureUtil::RemoveAllSignatures(const System::String &srcFileName, const System::String &dstFileName)
```


## Esempi



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

* Class [DigitalSignatureUtil](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
## DigitalSignatureUtil::RemoveAllSignatures(std::basic_istream\<CharType, Traits\>\&, std::basic_ostream\<CharType, Traits\>\&) method




```cpp
template<typename CharType,typename Traits> static void Aspose::Words::DigitalSignatures::DigitalSignatureUtil::RemoveAllSignatures(std::basic_istream<CharType, Traits> &srcStream, std::basic_ostream<CharType, Traits> &dstStream)
```

## Vedi anche

* Class [DigitalSignatureUtil](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
