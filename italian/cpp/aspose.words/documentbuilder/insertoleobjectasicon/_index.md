---
title: "Metodo Aspose::Words::DocumentBuilder::InsertOleObjectAsIcon"
linktitle: "InsertOleObjectAsIcon"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::DocumentBuilder::InsertOleObjectAsIcon. Inserisce un oggetto OLE incorporato come icona da uno stream nel documento. Consente di specificare il file icona e la didascalia. Rileva il tipo di oggetto OLE usando il parametro progID fornito in C++."
type: docs
weight: 42000
url: /it/cpp/aspose.words/documentbuilder/insertoleobjectasicon/
---
## DocumentBuilder::InsertOleObjectAsIcon(const System::SharedPtr\<System::IO::Stream\>\&, const System::String\&, const System::String\&, const System::String\&) method


Inserisce un oggetto OLE incorporato come icona da un flusso nel documento. Consente di specificare il file icona e la didascalia. Rileva il tipo di oggetto OLE usando il parametro progID fornito.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOleObjectAsIcon(const System::SharedPtr<System::IO::Stream> &stream, const System::String &progId, const System::String &iconFile, const System::String &iconCaption)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| flusso | const System::SharedPtr\<System::IO::Stream\>\& | Stream contenente i dati dell'applicazione. |
| progId | const System::String\& | ProgId dell'oggetto OLE. |
| iconFile | const System::String\& | Percorso completo del file ICO. Se il valore è **null**, Aspose.Words utilizzerà un'immagine predefinita. |
| iconCaption | const System::String\& | Didascalia dell'icona. Se il valore è **null**, Aspose.Words utilizzerà una didascalia dell'icona predefinita. |

### ReturnValue

Nodo forma contenente l'oggetto Ole e inserito nella posizione corrente del Builder.

## Esempi



Mostra come inserire un oggetto OLE incorporato o collegato come icona nel documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Se 'iconFile' e 'iconCaption' sono omessi, questo metodo sovraccaricato seleziona
// l'icona in base a 'progId' e utilizza il nome file per la didascalia dell'icona.
builder->InsertOleObjectAsIcon(get_MyDir() + u"Presentation.pptx", u"Package", false, get_ImageDir() + u"Logo icon.ico", u"My embedded file");

builder->InsertBreak(Aspose::Words::BreakType::LineBreak);

{
    auto stream = System::MakeObject<System::IO::FileStream>(get_MyDir() + u"Presentation.pptx", System::IO::FileMode::Open);
    // Se 'iconFile' e 'iconCaption' sono omessi, questo metodo sovraccaricato seleziona
    // l'icona in base all'estensione del file e utilizza il nome file per la didascalia dell'icona.
    System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertOleObjectAsIcon(stream, u"PowerPoint.Application", get_ImageDir() + u"Logo icon.ico", u"My embedded file stream");

    System::SharedPtr<Aspose::Words::Drawing::OlePackage> setOlePackage = shape->get_OleFormat()->get_OlePackage();
    setOlePackage->set_FileName(u"Presentation.pptx");
    setOlePackage->set_DisplayName(u"Presentation.pptx");
}

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertOleObjectAsIcon.docx");
```

## Vedi anche

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertOleObjectAsIcon(const System::String\&, bool, const System::String\&, const System::String\&) method


Inserisce un oggetto OLE incorporato o collegato come icona nel documento. Consente di specificare il file icona e la didascalia. Rileva il tipo di oggetto OLE usando l'estensione del file.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOleObjectAsIcon(const System::String &fileName, bool isLinked, const System::String &iconFile, const System::String &iconCaption)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| nomeFile | const System::String\& | Percorso completo del file. |
| isLinked | bool | Se **true** allora viene inserito un oggetto OLE collegato, altrimenti viene inserito un oggetto OLE incorporato. |
| iconFile | const System::String\& | Percorso completo del file ICO. Se il valore è **null**, Aspose.Words utilizzerà un'immagine predefinita. |
| iconCaption | const System::String\& | Didascalia dell'icona. Se il valore è **null**, Aspose.Words utilizzerà il nome del file. |

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
## DocumentBuilder::InsertOleObjectAsIcon(const System::String\&, const System::String\&, bool, const System::String\&, const System::String\&) method


Inserisce un oggetto OLE incorporato o collegato come icona nel documento. Consente di specificare il file icona e la didascalia. Rileva il tipo di oggetto OLE usando il parametro progID fornito.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOleObjectAsIcon(const System::String &fileName, const System::String &progId, bool isLinked, const System::String &iconFile, const System::String &iconCaption)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| nomeFile | const System::String\& | Percorso completo del file. |
| progId | const System::String\& | ProgId dell'oggetto OLE. |
| isLinked | bool | Se **true** allora viene inserito un oggetto OLE collegato, altrimenti viene inserito un oggetto OLE incorporato. |
| iconFile | const System::String\& | Percorso completo del file ICO. Se il valore è **null**, Aspose.Words utilizzerà un'immagine predefinita. |
| iconCaption | const System::String\& | Didascalia dell'icona. Se il valore è **null**, Aspose.Words utilizzerà il nome del file. |

### ReturnValue

Nodo forma contenente l'oggetto Ole e inserito nella posizione corrente del Builder.

## Esempi



Mostra come inserire un oggetto OLE incorporato o collegato come icona nel documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Se 'iconFile' e 'iconCaption' sono omessi, questo metodo sovraccaricato seleziona
// l'icona in base a 'progId' e utilizza il nome file per la didascalia dell'icona.
builder->InsertOleObjectAsIcon(get_MyDir() + u"Presentation.pptx", u"Package", false, get_ImageDir() + u"Logo icon.ico", u"My embedded file");

builder->InsertBreak(Aspose::Words::BreakType::LineBreak);

{
    auto stream = System::MakeObject<System::IO::FileStream>(get_MyDir() + u"Presentation.pptx", System::IO::FileMode::Open);
    // Se 'iconFile' e 'iconCaption' sono omessi, questo metodo sovraccaricato seleziona
    // l'icona in base all'estensione del file e utilizza il nome file per la didascalia dell'icona.
    System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertOleObjectAsIcon(stream, u"PowerPoint.Application", get_ImageDir() + u"Logo icon.ico", u"My embedded file stream");

    System::SharedPtr<Aspose::Words::Drawing::OlePackage> setOlePackage = shape->get_OleFormat()->get_OlePackage();
    setOlePackage->set_FileName(u"Presentation.pptx");
    setOlePackage->set_DisplayName(u"Presentation.pptx");
}

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertOleObjectAsIcon.docx");
```

## Vedi anche

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertOleObjectAsIcon(std::basic_istream\<CharType, Traits\>\&, System::String, System::String, System::String) method




```cpp
template<typename CharType,typename Traits> System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOleObjectAsIcon(std::basic_istream<CharType, Traits> &stream, System::String progId, System::String iconFile, System::String iconCaption)
```

## Vedi anche

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
