---
title: "Aspose::Words::Drawing::OleFormat::Save metodo"
linktitle: "Save"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::OleFormat::Save metodo. Salva i dati dell'oggetto incorporato nello stream specificato in C++."
type: docs
weight: 19000
url: /it/cpp/aspose.words.drawing/oleformat/save/
---
## OleFormat::Save(const System::SharedPtr\<System::IO::Stream\>\&) method


Salva i dati dell'oggetto incorporato nello stream specificato.

```cpp
void Aspose::Words::Drawing::OleFormat::Save(const System::SharedPtr<System::IO::Stream> &stream)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| flusso | const System::SharedPtr\<System::IO::Stream\>\& | Dove salvare i dati dell'oggetto. |
## Note


È responsabilità del chiamante rilasciare lo stream.

## Esempi



Mostra come estrarre oggetti OLE incorporati in file.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"OLE spreadsheet.docm");
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

// L'oggetto OLE nella prima forma è un foglio di calcolo Microsoft Excel.
System::SharedPtr<Aspose::Words::Drawing::OleFormat> oleFormat = shape->get_OleFormat();

ASSERT_EQ(u"Excel.Sheet.12", oleFormat->get_ProgId());

// Il nostro oggetto non è né in aggiornamento automatico né bloccato dagli aggiornamenti.
ASSERT_FALSE(oleFormat->get_AutoUpdate());
ASPOSE_ASSERT_EQ(false, oleFormat->get_IsLocked());

// Se prevediamo di salvare l'oggetto OLE in un file nel file system locale,
// possiamo utilizzare la proprietà "SuggestedExtension" per determinare quale estensione di file applicare al file.
ASSERT_EQ(u".xlsx", oleFormat->get_SuggestedExtension());

// Di seguito sono riportati due modi per salvare un oggetto OLE in un file nel file system locale.
// 1 -  Salvalo tramite uno stream:
{
    auto fs = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + u"OLE spreadsheet extracted via stream" + oleFormat->get_SuggestedExtension(), System::IO::FileMode::Create);
    oleFormat->Save(fs);
}

// 2 -  Salvalo direttamente in un nome file:
oleFormat->Save(get_ArtifactsDir() + u"OLE spreadsheet saved directly" + oleFormat->get_SuggestedExtension());
```

## Vedi anche

* Class [OleFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
## OleFormat::Save(const System::String\&) method


Salva i dati dell'oggetto incorporato in un file con il nome specificato.

```cpp
void Aspose::Words::Drawing::OleFormat::Save(const System::String &fileName)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| nomeFile | const System::String\& | Nome del file per salvare i dati dell'oggetto OLE. |

## Esempi



Mostra come estrarre oggetti OLE incorporati in file.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"OLE spreadsheet.docm");
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

// L'oggetto OLE nella prima forma è un foglio di calcolo Microsoft Excel.
System::SharedPtr<Aspose::Words::Drawing::OleFormat> oleFormat = shape->get_OleFormat();

ASSERT_EQ(u"Excel.Sheet.12", oleFormat->get_ProgId());

// Il nostro oggetto non è né in aggiornamento automatico né bloccato dagli aggiornamenti.
ASSERT_FALSE(oleFormat->get_AutoUpdate());
ASPOSE_ASSERT_EQ(false, oleFormat->get_IsLocked());

// Se prevediamo di salvare l'oggetto OLE in un file nel file system locale,
// possiamo utilizzare la proprietà "SuggestedExtension" per determinare quale estensione di file applicare al file.
ASSERT_EQ(u".xlsx", oleFormat->get_SuggestedExtension());

// Di seguito sono riportati due modi per salvare un oggetto OLE in un file nel file system locale.
// 1 -  Salvalo tramite uno stream:
{
    auto fs = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + u"OLE spreadsheet extracted via stream" + oleFormat->get_SuggestedExtension(), System::IO::FileMode::Create);
    oleFormat->Save(fs);
}

// 2 -  Salvalo direttamente in un nome file:
oleFormat->Save(get_ArtifactsDir() + u"OLE spreadsheet saved directly" + oleFormat->get_SuggestedExtension());
```

## Vedi anche

* Class [OleFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
## OleFormat::Save(std::basic_ostream\<CharType, Traits\>\&) method




```cpp
template<typename CharType,typename Traits> void Aspose::Words::Drawing::OleFormat::Save(std::basic_ostream<CharType, Traits> &stream)
```

## Vedi anche

* Class [OleFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
