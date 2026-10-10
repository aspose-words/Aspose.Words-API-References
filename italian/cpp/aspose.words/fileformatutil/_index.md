---
title: "Aspose::Words::FileFormatUtil classe"
linktitle: "FileFormatUtil"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::FileFormatUtil classe. Fornisce metodi di utilità per lavorare con i formati di file, come il rilevamento del formato o la conversione delle estensioni dei file da/a enum dei formati di file. Per saperne di più, visita l'articolo della documentazione in C++."
type: docs
weight: 28000
url: /it/cpp/aspose.words/fileformatutil/
---
## FileFormatUtil class


Fornisce metodi di utilità per lavorare con i formati di file, come il rilevamento del formato di file o la conversione delle estensioni di file da/a enum dei formati di file. Per saperne di più, visita l'articolo di documentazione [Detect File Format and Check Format Compatibility](https://docs.aspose.com/words/cpp/detect-file-format-and-check-format-compatibility/).

```cpp
class FileFormatUtil
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| static [ContentTypeToLoadFormat](./contenttypetoloadformat/)(const System::String\&) | Converte il tipo di contenuto IANA in un valore enumerato di formato di caricamento. |
| static [ContentTypeToSaveFormat](./contenttypetosaveformat/)(const System::String\&) | Converte il tipo di contenuto IANA in un valore enumerato di formato di salvataggio. |
| static [DetectFileFormat](./detectfileformat/)(const System::String\&) | Rileva e restituisce le informazioni su un formato di un documento memorizzato in un file su disco. |
| static [DetectFileFormat](./detectfileformat/)(const System::SharedPtr\<System::IO::Stream\>\&) | Rileva e restituisce le informazioni su un formato di un documento memorizzato in uno stream. |
| static [DetectFileFormat](./detectfileformat/)(std::basic_istream\<CharType, Traits\>\&) |  |
| static [ExtensionToSaveFormat](./extensiontosaveformat/)(const System::String\&) | Converte un'estensione di nome file in un valore [SaveFormat](../saveformat/). |
| [FileFormatUtil](./fileformatutil/)() |  |
| static [ImageTypeToExtension](./imagetypetoextension/)(Aspose::Words::Drawing::ImageType) | Converte un valore enumerato di tipo immagine Aspose.Words in un'estensione di file. L'estensione restituita è una stringa in minuscolo con un punto iniziale. |
| static [LoadFormatToExtension](./loadformattoextension/)(Aspose::Words::LoadFormat) | Converte un valore enumerato di formato di caricamento in un'estensione di file. L'estensione restituita è una stringa in minuscolo con un punto iniziale. |
| static [LoadFormatToSaveFormat](./loadformattosaveformat/)(Aspose::Words::LoadFormat) | Converte un valore [LoadFormat](../loadformat/) in un valore [SaveFormat](../saveformat/) se possibile. |
| static [SaveFormatToExtension](./saveformattoextension/)(Aspose::Words::SaveFormat) | Converte un valore enumerato di formato di salvataggio in un'estensione di file. L'estensione restituita è una stringa in minuscolo con un punto iniziale. |
| static [SaveFormatToLoadFormat](./saveformattoloadformat/)(Aspose::Words::SaveFormat) | Converte un valore [SaveFormat](../saveformat/) in un valore [LoadFormat](../loadformat/) se possibile. |

## Esempi



Mostra come rilevare la codifica in un file html.
```cpp
System::SharedPtr<Aspose::Words::FileFormatInfo> info = Aspose::Words::FileFormatUtil::DetectFileFormat(get_MyDir() + u"Document.html");

ASSERT_EQ(Aspose::Words::LoadFormat::Html, info->get_LoadFormat());

// La proprietà Encoding è usata solo quando creiamo un oggetto FileFormatInfo per un documento html.
ASSERT_EQ(u"Western European (Windows)", info->get_Encoding()->get_EncodingName());
ASSERT_EQ(1252, info->get_Encoding()->get_CodePage());
```

## Vedi anche

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
