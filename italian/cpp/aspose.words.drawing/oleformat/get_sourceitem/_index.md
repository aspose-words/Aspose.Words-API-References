---
title: "Aspose::Words::Drawing::OleFormat::get_SourceItem metodo"
linktitle: "get_SourceItem"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::OleFormat::get_SourceItem metodo. Ottiene o imposta una stringa utilizzata per identificare la parte del file di origine che è collegata in C++."
type: docs
weight: 12000
url: /it/cpp/aspose.words.drawing/oleformat/get_sourceitem/
---
## OleFormat::get_SourceItem method


Ottiene o imposta una stringa usata per identificare la porzione del file sorgente che viene collegata.

```cpp
System::String Aspose::Words::Drawing::OleFormat::get_SourceItem()
```

## Note


Il valore predefinito è una stringa vuota.

Ad esempio, se il file di origine è una cartella di lavoro Microsoft Excel, la proprietà [SourceItem](./) potrebbe restituire "Workbook1!R3C1:R4C2" se l'oggetto OLE contiene solo alcune celle del foglio di lavoro.

## Esempi



Mostra come inserire oggetti OLE collegati e non collegati.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Incorpora un disegno Microsoft Visio nel documento come oggetto OLE.
builder->InsertOleObject(get_ImageDir() + u"Microsoft Visio drawing.vsd", u"Package", false, false, nullptr);

// Inserisci un collegamento al file nel file system locale e visualizzalo come icona.
builder->InsertOleObject(get_ImageDir() + u"Microsoft Visio drawing.vsd", u"Package", true, true, nullptr);

// L'inserimento di oggetti OLE crea forme che memorizzano questi oggetti.
System::ArrayPtr<System::SharedPtr<Aspose::Words::Drawing::Shape>> shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()->LINQ_ToArray();

ASSERT_EQ(2, shapes->get_Length());
ASSERT_EQ(2, shapes->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Drawing::Shape>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Drawing::Shape> s)>>([](System::SharedPtr<Aspose::Words::Drawing::Shape> s) -> bool
{
    return s->get_ShapeType() == Aspose::Words::Drawing::ShapeType::OleObject;
}))));

// Se una forma contiene un oggetto OLE, avrà una proprietà "OleFormat" valida,
// che possiamo usare per verificare alcuni aspetti della forma.
System::SharedPtr<Aspose::Words::Drawing::OleFormat> oleFormat = shapes[0]->get_OleFormat();

ASPOSE_ASSERT_EQ(false, oleFormat->get_IsLink());
ASPOSE_ASSERT_EQ(false, oleFormat->get_OleIcon());

oleFormat = shapes[1]->get_OleFormat();

ASPOSE_ASSERT_EQ(true, oleFormat->get_IsLink());
ASPOSE_ASSERT_EQ(true, oleFormat->get_OleIcon());

ASSERT_TRUE(oleFormat->get_SourceFullName().EndsWith(System::String(u"Images") + System::IO::Path::DirectorySeparatorChar + u"Microsoft Visio drawing.vsd"));
ASSERT_EQ(u"", oleFormat->get_SourceItem());

ASSERT_EQ(u"Microsoft Visio drawing.vsd", oleFormat->get_IconCaption());

doc->Save(get_ArtifactsDir() + u"Shape.OleLinks.docx");

// Se l'oggetto contiene dati OLE, possiamo accedervi usando un flusso.
{
    System::SharedPtr<System::IO::MemoryStream> stream = oleFormat->GetOleEntry(u"\x0001" u"CompObj");
    System::ArrayPtr<uint8_t> oleEntryBytes = stream->ToArray();
    ASSERT_EQ(76, oleEntryBytes->get_Length());
}
```

## Vedi anche

* Class [OleFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
