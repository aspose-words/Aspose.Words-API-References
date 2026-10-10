---
title: "Aspose::Words::DigitalSignatures::DigitalSignatureUtil classe"
linktitle: "DigitalSignatureUtil"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::DigitalSignatures::DigitalSignatureUtil classe. Fornisce metodi per firmare il documento. Per saperne di più, visita l'articolo della documentazione in C++."
type: docs
weight: 4000
url: /it/cpp/aspose.words.digitalsignatures/digitalsignatureutil/
---
## DigitalSignatureUtil class


Fornisce metodi per firmare un documento. Per saperne di più, visita l'articolo di documentazione [Work with Digital Signatures](https://docs.aspose.com/words/cpp/working-with-digital-signatures/).

```cpp
class DigitalSignatureUtil
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [DigitalSignatureUtil](./digitalsignatureutil/)() |  |
| static [LoadSignatures](./loadsignatures/)(const System::String\&) | Carica le firme digitali dal documento. |
| static [LoadSignatures](./loadsignatures/)(const System::SharedPtr\<System::IO::Stream\>\&) | Carica le firme digitali dal documento usando lo stream. |
| static [LoadSignatures](./loadsignatures/)(std::basic_istream\<CharType, Traits\>\&) |  |
| static [RemoveAllSignatures](./removeallsignatures/)(const System::String\&, const System::String\&) | Rimuove tutte le firme digitali dal file di origine e scrive il file non firmato nel file di destinazione. I seguenti formati sono compatibili per la rimozione della firma digitale: [Doc](../../aspose.words/loadformat/), [Dot](../../aspose.words/loadformat/), [Docx](../../aspose.words/loadformat/), [Dotx](../../aspose.words/loadformat/), [Docm](../../aspose.words/loadformat/), [Dotm](../../aspose.words/loadformat/), [Odt](../../aspose.words/loadformat/), [Ott](../../aspose.words/loadformat/). |
| static [RemoveAllSignatures](./removeallsignatures/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&) | Rimuove tutte le firme digitali dal documento nello stream di origine e scrive il documento non firmato nello stream di destinazione. **L'output verrà scritto all'inizio dello stream e la dimensione dello stream verrà aggiornata con la lunghezza del contenuto.** I seguenti formati sono compatibili per la rimozione della firma digitale: [Doc](../../aspose.words/loadformat/), [Dot](../../aspose.words/loadformat/), [Docx](../../aspose.words/loadformat/), [Dotx](../../aspose.words/loadformat/), [Docm](../../aspose.words/loadformat/), [Dotm](../../aspose.words/loadformat/), [Odt](../../aspose.words/loadformat/), [Ott](../../aspose.words/loadformat/). |
| static [RemoveAllSignatures](./removeallsignatures/)(std::basic_istream\<CharType, Traits\>\&, std::basic_ostream\<CharType, Traits\>\&) |  |
| static [Sign](./sign/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\&, const System::SharedPtr\<Aspose::Words::DigitalSignatures::SignOptions\>\&) | Firma il documento di origine usando il [CertificateHolder](../certificateholder/) e il [SignOptions](../signoptions/) forniti con firma digitale e scrive il documento firmato nello stream di destinazione. I formati supportati sono: [Doc](../../aspose.words/loadformat/), [Dot](../../aspose.words/loadformat/), [Docx](../../aspose.words/loadformat/), [Dotx](../../aspose.words/loadformat/), [Docm](../../aspose.words/loadformat/), [Dotm](../../aspose.words/loadformat/), [Odt](../../aspose.words/loadformat/), [Ott](../../aspose.words/loadformat/). **L'output verrà scritto all'inizio dello stream e la dimensione dello stream verrà aggiornata con la lunghezza del contenuto.** |
| static [Sign](./sign/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\&, const System::SharedPtr\<Aspose::Words::DigitalSignatures::SignOptions\>\&) | Firma il documento di origine usando il [CertificateHolder](../certificateholder/) e il [SignOptions](../signoptions/) forniti con firma digitale e scrive il documento firmato nel file di destinazione. I formati supportati sono: [Doc](../../aspose.words/loadformat/), [Dot](../../aspose.words/loadformat/), [Docx](../../aspose.words/loadformat/), [Dotx](../../aspose.words/loadformat/), [Docm](../../aspose.words/loadformat/), [Dotm](../../aspose.words/loadformat/), [Odt](../../aspose.words/loadformat/), [Ott](../../aspose.words/loadformat/). |
| static [Sign](./sign/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\&) | Firma il documento di origine usando il [CertificateHolder](../certificateholder/) fornito con firma digitale e scrive il documento firmato nello stream di destinazione. I formati supportati sono: [Doc](../../aspose.words/loadformat/), [Dot](../../aspose.words/loadformat/), [Docx](../../aspose.words/loadformat/), [Dotx](../../aspose.words/loadformat/), [Docm](../../aspose.words/loadformat/), [Dotm](../../aspose.words/loadformat/), [Odt](../../aspose.words/loadformat/), [Ott](../../aspose.words/loadformat/). **L'output verrà scritto all'inizio dello stream e la dimensione dello stream verrà aggiornata con la lunghezza del contenuto.** |
| static [Sign](./sign/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\&) | Firma il documento di origine usando il [CertificateHolder](../certificateholder/) fornito con firma digitale e scrive il documento firmato nel file di destinazione. I formati supportati sono: [Doc](../../aspose.words/loadformat/), [Dot](../../aspose.words/loadformat/), [Docx](../../aspose.words/loadformat/), [Dotx](../../aspose.words/loadformat/), [Docm](../../aspose.words/loadformat/), [Dotm](../../aspose.words/loadformat/), [Odt](../../aspose.words/loadformat/), [Ott](../../aspose.words/loadformat/). |
| static [Sign](./sign/)(std::basic_istream\<CharType, Traits\>\&, std::basic_ostream\<CharType, Traits\>\&, System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>, System::SharedPtr\<Aspose::Words::DigitalSignatures::SignOptions\>) |  |
| static [Sign](./sign/)(std::basic_istream\<CharType, Traits\>\&, std::basic_ostream\<CharType, Traits\>\&, System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>) |  |
## Note


Poiché la firma digitale funziona con il contenuto del file anziché con il modello a oggetti [Document](../../aspose.words/document/), questi metodi sono inseriti in una classe separata.

I formati supportati sono: [Doc](../../aspose.words/loadformat/), [Dot](../../aspose.words/loadformat/), [Docx](../../aspose.words/loadformat/), [Dotx](../../aspose.words/loadformat/), [Docm](../../aspose.words/loadformat/), [Dotm](../../aspose.words/loadformat/), [Odt](../../aspose.words/loadformat/), [Ott](../../aspose.words/loadformat/).

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

* Namespace [Aspose::Words::DigitalSignatures](../)
* Library [Aspose.Words for C++](../../)
