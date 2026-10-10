---
title: "Aspose::Words::DocumentBuilder::InsertOleObject method"
linktitle: "InsertOleObject"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::DocumentBuilder::InsertOleObject method. Inserisce un oggetto OLE incorporato da uno stream nel documento in C++."
type: docs
weight: 41000
url: /it/cpp/aspose.words/documentbuilder/insertoleobject/
---
## DocumentBuilder::InsertOleObject(const System::SharedPtr\<System::IO::Stream\>\&, const System::String\&, bool, const System::SharedPtr\<System::IO::Stream\>\&) method


Inserisce un oggetto OLE incorporato da un flusso nel documento.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOleObject(const System::SharedPtr<System::IO::Stream> &stream, const System::String &progId, bool asIcon, const System::SharedPtr<System::IO::Stream> &presentation)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| flusso | const System::SharedPtr\<System::IO::Stream\>\& | Stream contenente i dati dell'applicazione. |
| progId | const System::String\& | Identificatore programmatico dell'oggetto OLE. |
| asIcon | bool | Specifica la modalità Iconic o Normal dell'oggetto OLE da inserire. |
| presentation | const System::SharedPtr\<System::IO::Stream\>\& | Presentazione immagine dell'oggetto OLE. Se il valore è **null** Aspose.Words utilizzerà una delle immagini predefinite. |

### ReturnValue

Nodo forma contenente l'oggetto Ole e inserito nella posizione corrente del Builder.

## Esempi



Mostra come utilizzare il document builder per incorporare oggetti OLE in un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserisci un foglio di calcolo Microsoft Excel dal file system locale
// nel documento mantenendo il suo aspetto predefinito.
{
    System::SharedPtr<System::IO::Stream> spreadsheetStream = System::IO::File::Open(get_MyDir() + u"Spreadsheet.xlsx", System::IO::FileMode::Open);
    builder->Writeln(u"Spreadsheet Ole object:");
    // Se 'presentation' è omesso e 'asIcon' è impostato, questo metodo sovraccaricato seleziona
    // l'icona in base a 'progId' e utilizza la didascalia dell'icona predefinita.
    builder->InsertOleObject(spreadsheetStream, u"OleObject.xlsx", false, nullptr);
}

// Inserisci una presentazione Microsoft Powerpoint come oggetto OLE.
// Questa volta, avrà un'immagine scaricata dal web per un'icona.
{
    System::SharedPtr<System::IO::Stream> powerpointStream = System::IO::File::Open(get_MyDir() + u"Presentation.pptx", System::IO::FileMode::Open);
    System::ArrayPtr<uint8_t> imgBytes = System::IO::File::ReadAllBytes(get_ImageDir() + u"Logo.jpg");

    {
        auto imageStream = System::MakeObject<System::IO::MemoryStream>(imgBytes);
        builder->InsertParagraph();
        builder->Writeln(u"Powerpoint Ole object:");
        builder->InsertOleObject(powerpointStream, u"OleObject.pptx", true, imageStream);
    }
}

// Fai doppio clic su questi oggetti in Microsoft Word per aprire
// i file collegati utilizzando le rispettive applicazioni.
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertOleObjects.docx");
```

## Vedi anche

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertOleObject(const System::String\&, bool, bool, const System::SharedPtr\<System::IO::Stream\>\&) method


Inserisce un oggetto OLE incorporato o collegato da un file nel documento. Rileva il tipo di oggetto OLE usando l'estensione del file.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOleObject(const System::String &fileName, bool isLinked, bool asIcon, const System::SharedPtr<System::IO::Stream> &presentation)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| nomeFile | const System::String\& | Percorso completo del file. |
| isLinked | bool | Se **true** allora viene inserito un oggetto OLE collegato, altrimenti viene inserito un oggetto OLE incorporato. |
| asIcon | bool | Specifica la modalità Iconic o Normal dell'oggetto OLE da inserire. |
| presentation | const System::SharedPtr\<System::IO::Stream\>\& | Presentazione immagine dell'oggetto OLE. Se il valore è **null** Aspose.Words utilizzerà una delle immagini predefinite. |

### ReturnValue

Nodo forma contenente l'oggetto Ole e inserito nella posizione corrente del Builder.

## Esempi



Mostra come inserire un oggetto OLE in un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Gli oggetti OLE sono collegamenti a file nel nostro file system locale che possono essere aperti da altre applicazioni installate.
// Doppio clic su queste forme avvierà l'applicazione e la utilizzerà per aprire l'oggetto collegato.
// Esistono tre modi per utilizzare il metodo InsertOleObject per inserire queste forme e configurare il loro aspetto.
// 1 -  Immagine presa dal file system locale:
{
    auto imageStream = System::MakeObject<System::IO::FileStream>(get_ImageDir() + u"Logo.jpg", System::IO::FileMode::Open);
    // Se 'presentation' è omesso e 'asIcon' è impostato, questo metodo sovraccaricato seleziona
    // l'icona in base all'estensione del file e utilizza il nome file per la didascalia dell'icona.
    builder->InsertOleObject(get_MyDir() + u"Spreadsheet.xlsx", false, false, imageStream);
}

// Se 'presentation' è omesso e 'asIcon' è impostato, questo metodo sovraccaricato seleziona
// l'icona in base a 'progId' e utilizza il nome file per la didascalia dell'icona.
// 2 -  Icona basata sull'applicazione che aprirà l'oggetto:
builder->InsertOleObject(get_MyDir() + u"Spreadsheet.xlsx", u"Excel.Sheet", false, true, nullptr);

// Se 'iconFile' e 'iconCaption' sono omessi, questo metodo sovraccaricato seleziona
// l'icona in base a 'progId' e utilizza la didascalia dell'icona predefinita.
// 3 -  Icona immagine di 32 x 32 pixel o più piccola dal file system locale, con una didascalia personalizzata:
builder->InsertOleObjectAsIcon(get_MyDir() + u"Presentation.pptx", false, get_ImageDir() + u"Logo icon.ico", u"Double click to view presentation!");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertOleObject.docx");
```

## Vedi anche

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertOleObject(const System::String\&, const System::String\&, bool, bool, const System::SharedPtr\<System::IO::Stream\>\&) method


Inserisce un oggetto OLE incorporato o collegato da un file nel documento. Rileva il tipo di oggetto OLE usando il parametro progID fornito.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOleObject(const System::String &fileName, const System::String &progId, bool isLinked, bool asIcon, const System::SharedPtr<System::IO::Stream> &presentation)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| nomeFile | const System::String\& | Percorso completo del file. |
| progId | const System::String\& | ProgId dell'oggetto OLE. |
| isLinked | bool | Se **true** allora viene inserito un oggetto OLE collegato, altrimenti viene inserito un oggetto OLE incorporato. |
| asIcon | bool | Specifica la modalità Iconic o Normal dell'oggetto OLE da inserire. |
| presentation | const System::SharedPtr\<System::IO::Stream\>\& | Presentazione immagine dell'oggetto OLE. Se il valore è **null** Aspose.Words utilizzerà una delle immagini predefinite. |

### ReturnValue

Nodo forma contenente l'oggetto Ole e inserito nella posizione corrente del Builder.

## Esempi



Mostra come inserire un oggetto OLE in un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Gli oggetti OLE sono collegamenti a file nel nostro file system locale che possono essere aperti da altre applicazioni installate.
// Doppio clic su queste forme avvierà l'applicazione e la utilizzerà per aprire l'oggetto collegato.
// Esistono tre modi per utilizzare il metodo InsertOleObject per inserire queste forme e configurare il loro aspetto.
// 1 -  Immagine presa dal file system locale:
{
    auto imageStream = System::MakeObject<System::IO::FileStream>(get_ImageDir() + u"Logo.jpg", System::IO::FileMode::Open);
    // Se 'presentation' è omesso e 'asIcon' è impostato, questo metodo sovraccaricato seleziona
    // l'icona in base all'estensione del file e utilizza il nome file per la didascalia dell'icona.
    builder->InsertOleObject(get_MyDir() + u"Spreadsheet.xlsx", false, false, imageStream);
}

// Se 'presentation' è omesso e 'asIcon' è impostato, questo metodo sovraccaricato seleziona
// l'icona in base a 'progId' e utilizza il nome file per la didascalia dell'icona.
// 2 -  Icona basata sull'applicazione che aprirà l'oggetto:
builder->InsertOleObject(get_MyDir() + u"Spreadsheet.xlsx", u"Excel.Sheet", false, true, nullptr);

// Se 'iconFile' e 'iconCaption' sono omessi, questo metodo sovraccaricato seleziona
// l'icona in base a 'progId' e utilizza la didascalia dell'icona predefinita.
// 3 -  Icona immagine di 32 x 32 pixel o più piccola dal file system locale, con una didascalia personalizzata:
builder->InsertOleObjectAsIcon(get_MyDir() + u"Presentation.pptx", false, get_ImageDir() + u"Logo icon.ico", u"Double click to view presentation!");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertOleObject.docx");
```

## Vedi anche

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertOleObject(std::basic_istream\<CharType, Traits\>\&, System::String, bool, std::basic_istream\<CharType, Traits\>\&) method




```cpp
template<typename CharType,typename Traits> System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOleObject(std::basic_istream<CharType, Traits> &stream, System::String progId, bool asIcon, std::basic_istream<CharType, Traits> &presentation)
```

## Vedi anche

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertOleObject(System::String, bool, bool, std::basic_istream\<CharType, Traits\>\&) method




```cpp
template<typename CharType,typename Traits> System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOleObject(System::String fileName, bool isLinked, bool asIcon, std::basic_istream<CharType, Traits> &presentation)
```

## Vedi anche

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertOleObject(System::String, System::String, bool, bool, std::basic_istream\<CharType, Traits\>\&) method




```cpp
template<typename CharType,typename Traits> System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOleObject(System::String fileName, System::String progId, bool isLinked, bool asIcon, std::basic_istream<CharType, Traits> &presentation)
```

## Vedi anche

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
