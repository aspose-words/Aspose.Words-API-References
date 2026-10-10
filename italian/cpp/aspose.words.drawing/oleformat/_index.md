---
title: "Classe Aspose::Words::Drawing::OleFormat"
linktitle: "OleFormat"
second_title: "Riferimento API Aspose.Words per C++"
description: "Classe Aspose::Words::Drawing::OleFormat. Fornisce l'accesso ai dati di un oggetto OLE o di un controllo ActiveX. Per saperne di più, visita l'articolo della documentazione in C++."
type: docs
weight: 8000
url: /it/cpp/aspose.words.drawing/oleformat/
---
## OleFormat class


Fornisce l'accesso ai dati di un oggetto OLE o di un controllo ActiveX. Per saperne di più, visita l'articolo di documentazione [Working with Ole Objects](https://docs.aspose.com/words/cpp/working-with-ole-objects/).

```cpp
class OleFormat : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get_AutoUpdate](./get_autoupdate/)() | Specifica se il collegamento all'oggetto OLE viene aggiornato automaticamente o meno in Microsoft Word. |
| [get_Clsid](./get_clsid/)() | Ottiene il CLSID dell'oggetto OLE. |
| [get_IconCaption](./get_iconcaption/)() | Ottiene la didascalia dell'icona dell'oggetto OLE. Nel caso in cui l'oggetto OLE non abbia un'icona o la didascalia non possa essere recuperata, restituisce una stringa vuota. |
| [get_IsLink](./get_islink/)() | Restituisce **true** se l'oggetto OLE è collegato (quando [SourceFullName](./get_sourcefullname/) è specificato). |
| [get_IsLocked](./get_islocked/)() | Specifica se il collegamento all'oggetto OLE è bloccato dagli aggiornamenti. |
| [get_OleControl](./get_olecontrol/)() | Ottiene gli oggetti [OleControl](./get_olecontrol/) se questo oggetto OLE è un controllo ActiveX. Altrimenti questa proprietà è null. |
| [get_OleIcon](./get_oleicon/)() | Ottiene l'aspetto di disegno dell'oggetto OLE. Quando **true**, l'oggetto OLE è visualizzato come icona. Quando **false**, l'oggetto OLE è visualizzato come contenuto. |
| [get_OlePackage](./get_olepackage/)() | Fornisce l'accesso a [OlePackage](../olepackage/) se l'oggetto OLE è un pacchetto OLE. Restituisce **null** altrimenti. |
| [get_ProgId](./get_progid/)() | Ottiene o imposta il ProgID dell'oggetto OLE. |
| [get_SourceFullName](./get_sourcefullname/)() | Ottiene o imposta il percorso e il nome del file sorgente per l'oggetto OLE collegato. |
| [get_SourceItem](./get_sourceitem/)() | Ottiene o imposta una stringa usata per identificare la porzione del file sorgente che viene collegata. |
| [get_SuggestedExtension](./get_suggestedextension/)() | Ottiene l'estensione del file suggerita per l'oggetto incorporato corrente se si desidera salvarlo in un file. |
| [get_SuggestedFileName](./get_suggestedfilename/)() | Ottiene il nome file suggerito per l'oggetto incorporato corrente se si desidera salvarlo in un file. |
| [GetOleEntry](./getoleentry/)(const System::String\&) | Ottiene la voce dei dati dell'oggetto OLE. |
| [GetRawData](./getrawdata/)() | Ottiene i dati grezzi dell'oggetto OLE. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Save](./save/)(const System::SharedPtr\<System::IO::Stream\>\&) | Salva i dati dell'oggetto incorporato nello stream specificato. |
| [Save](./save/)(const System::String\&) | Salva i dati dell'oggetto incorporato in un file con il nome specificato. |
| [Save](./save/)(std::basic_ostream\<CharType, Traits\>\&) |  |
| [set_AutoUpdate](./set_autoupdate/)(bool) | Metodo set per [Aspose::Words::Drawing::OleFormat::get_AutoUpdate](./get_autoupdate/). |
| [set_IsLocked](./set_islocked/)(bool) | Metodo set per [Aspose::Words::Drawing::OleFormat::get_IsLocked](./get_islocked/). |
| [set_ProgId](./set_progid/)(const System::String\&) | Metodo set per [Aspose::Words::Drawing::OleFormat::get_ProgId](./get_progid/). |
| [set_SourceFullName](./set_sourcefullname/)(const System::String\&) | Metodo set per [Aspose::Words::Drawing::OleFormat::get_SourceFullName](./get_sourcefullname/). |
| [set_SourceItem](./set_sourceitem/)(const System::String\&) | Metodo set per [Aspose::Words::Drawing::OleFormat::get_SourceItem](./get_sourceitem/). |
| static [Type](./type/)() |  |
## Note


Utilizza la proprietà [OleFormat](../shape/get_oleformat/) per accedere ai dati di un oggetto OLE. Non crei istanze della classe [OleFormat](./) direttamente.

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

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
