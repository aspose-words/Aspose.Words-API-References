---
title: "Aspose::Words::DocumentBuilder::InsertOleObject‑metod"
linktitle: "InsertOleObject"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::DocumentBuilder::InsertOleObject‑metod. Infogar ett inbäddat OLE‑objekt från en ström i dokumentet i C++."
type: docs
weight: 41000
url: /sv/cpp/aspose.words/documentbuilder/insertoleobject/
---
## DocumentBuilder::InsertOleObject(const System::SharedPtr\<System::IO::Stream\>\&, const System::String\&, bool, const System::SharedPtr\<System::IO::Stream\>\&) method


Infogar ett inbäddat OLE-objekt från en ström i dokumentet.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOleObject(const System::SharedPtr<System::IO::Stream> &stream, const System::String &progId, bool asIcon, const System::SharedPtr<System::IO::Stream> &presentation)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| ström | const System::SharedPtr\<System::IO::Stream\>\& | Ström som innehåller programdata. |
| progId | const System::String\& | Programmatisk identifierare för OLE‑objekt. |
| asIcon | bool | Anger antingen ikon‑ eller normalt läge för det OLE‑objekt som infogas. |
| presentation | const System::SharedPtr\<System::IO::Stream\>\& | Bildpresentation av OLE-objekt. Om värdet är **null** kommer Aspose.Words att använda en av de fördefinierade bilderna. |

### ReturnValue

Formnod som innehåller Ole-objekt och infogas på den aktuella Builder‑positionen.

## Exempel



Visar hur man använder dokumentbyggaren för att bädda in OLE-objekt i ett dokument.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Infoga ett Microsoft Excel-kalkylblad från det lokala filsystemet
// i dokumentet samtidigt som dess standardutseende behålls.
{
    System::SharedPtr<System::IO::Stream> spreadsheetStream = System::IO::File::Open(get_MyDir() + u"Spreadsheet.xlsx", System::IO::FileMode::Open);
    builder->Writeln(u"Spreadsheet Ole object:");
    // Om 'presentation' utelämnas och 'asIcon' är satt, väljer den här överlagrade metoden
    // ikonen enligt 'progId' och använder den fördefinierade ikontexten.
    builder->InsertOleObject(spreadsheetStream, u"OleObject.xlsx", false, nullptr);
}

// Infoga en Microsoft Powerpoint-presentation som ett OLE-objekt.
// Den här gången kommer den att ha en bild hämtad från webben som en ikon.
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

// Dubbelklicka på dessa objekt i Microsoft Word för att öppna
// de länkade filerna med deras respektive program.
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertOleObjects.docx");
```

## Se även

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertOleObject(const System::String\&, bool, bool, const System::SharedPtr\<System::IO::Stream\>\&) method


Infogar ett inbäddat eller länkat OLE-objekt från en fil i dokumentet. Detekterar OLE-objekttyp med hjälp av filändelse.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOleObject(const System::String &fileName, bool isLinked, bool asIcon, const System::SharedPtr<System::IO::Stream> &presentation)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| fileName | const System::String\& | Fullständig sökväg till filen. |
| isLinked | bool | Om **true** så infogas ett länkat OLE-objekt, annars infogas ett inbäddat OLE-objekt. |
| asIcon | bool | Anger antingen ikon‑ eller normalt läge för det OLE‑objekt som infogas. |
| presentation | const System::SharedPtr\<System::IO::Stream\>\& | Bildpresentation av OLE-objekt. Om värdet är **null** kommer Aspose.Words att använda en av de fördefinierade bilderna. |

### ReturnValue

Formnod som innehåller Ole-objekt och infogas på den aktuella Builder‑positionen.

## Exempel



Visar hur man infogar ett OLE-objekt i ett dokument.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// OLE-objekt är länkar till filer i vårt lokala filsystem som kan öppnas av andra installerade program.
// Dubbelklick på dessa former startar programmet och använder det sedan för att öppna det länkade objektet.
// Det finns tre sätt att använda metoden InsertOleObject för att infoga dessa former och konfigurera deras utseende.
// 1 -  Bild hämtad från det lokala filsystemet:
{
    auto imageStream = System::MakeObject<System::IO::FileStream>(get_ImageDir() + u"Logo.jpg", System::IO::FileMode::Open);
    // Om 'presentation' utelämnas och 'asIcon' är satt, väljer den här överlagrade metoden
    // ikonen enligt filändelsen och använder filnamnet som ikontext.
    builder->InsertOleObject(get_MyDir() + u"Spreadsheet.xlsx", false, false, imageStream);
}

// Om 'presentation' utelämnas och 'asIcon' är satt, väljer den här överlagrade metoden
// ikonen enligt 'progId' och använder filnamnet som ikontext.
// 2 -  Ikon baserad på programmet som kommer att öppna objektet:
builder->InsertOleObject(get_MyDir() + u"Spreadsheet.xlsx", u"Excel.Sheet", false, true, nullptr);

// Om 'iconFile' och 'iconCaption' utelämnas, väljer denna överlagrade metod
// ikonen enligt 'progId' och använder den fördefinierade ikontexten.
// 3 -  Bildikon som är 32 x 32 pixlar eller mindre från det lokala filsystemet, med en anpassad text:
builder->InsertOleObjectAsIcon(get_MyDir() + u"Presentation.pptx", false, get_ImageDir() + u"Logo icon.ico", u"Double click to view presentation!");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertOleObject.docx");
```

## Se även

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertOleObject(const System::String\&, const System::String\&, bool, bool, const System::SharedPtr\<System::IO::Stream\>\&) method


Infogar ett inbäddat eller länkat OLE-objekt från en fil i dokumentet. Detekterar OLE-objekttyp med hjälp av angivet progID-parameter.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOleObject(const System::String &fileName, const System::String &progId, bool isLinked, bool asIcon, const System::SharedPtr<System::IO::Stream> &presentation)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| fileName | const System::String\& | Fullständig sökväg till filen. |
| progId | const System::String\& | ProgId för OLE-objekt. |
| isLinked | bool | Om **true** så infogas ett länkat OLE-objekt, annars infogas ett inbäddat OLE-objekt. |
| asIcon | bool | Anger antingen ikon‑ eller normalt läge för det OLE‑objekt som infogas. |
| presentation | const System::SharedPtr\<System::IO::Stream\>\& | Bildpresentation av OLE-objekt. Om värdet är **null** kommer Aspose.Words att använda en av de fördefinierade bilderna. |

### ReturnValue

Formnod som innehåller Ole-objekt och infogas på den aktuella Builder‑positionen.

## Exempel



Visar hur man infogar ett OLE-objekt i ett dokument.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// OLE-objekt är länkar till filer i vårt lokala filsystem som kan öppnas av andra installerade program.
// Dubbelklick på dessa former startar programmet och använder det sedan för att öppna det länkade objektet.
// Det finns tre sätt att använda metoden InsertOleObject för att infoga dessa former och konfigurera deras utseende.
// 1 -  Bild hämtad från det lokala filsystemet:
{
    auto imageStream = System::MakeObject<System::IO::FileStream>(get_ImageDir() + u"Logo.jpg", System::IO::FileMode::Open);
    // Om 'presentation' utelämnas och 'asIcon' är satt, väljer den här överlagrade metoden
    // ikonen enligt filändelsen och använder filnamnet som ikontext.
    builder->InsertOleObject(get_MyDir() + u"Spreadsheet.xlsx", false, false, imageStream);
}

// Om 'presentation' utelämnas och 'asIcon' är satt, väljer den här överlagrade metoden
// ikonen enligt 'progId' och använder filnamnet som ikontext.
// 2 -  Ikon baserad på programmet som kommer att öppna objektet:
builder->InsertOleObject(get_MyDir() + u"Spreadsheet.xlsx", u"Excel.Sheet", false, true, nullptr);

// Om 'iconFile' och 'iconCaption' utelämnas, väljer denna överlagrade metod
// ikonen enligt 'progId' och använder den fördefinierade ikontexten.
// 3 -  Bildikon som är 32 x 32 pixlar eller mindre från det lokala filsystemet, med en anpassad text:
builder->InsertOleObjectAsIcon(get_MyDir() + u"Presentation.pptx", false, get_ImageDir() + u"Logo icon.ico", u"Double click to view presentation!");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertOleObject.docx");
```

## Se även

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertOleObject(std::basic_istream\<CharType, Traits\>\&, System::String, bool, std::basic_istream\<CharType, Traits\>\&) method




```cpp
template<typename CharType,typename Traits> System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOleObject(std::basic_istream<CharType, Traits> &stream, System::String progId, bool asIcon, std::basic_istream<CharType, Traits> &presentation)
```

## Se även

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertOleObject(System::String, bool, bool, std::basic_istream\<CharType, Traits\>\&) method




```cpp
template<typename CharType,typename Traits> System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOleObject(System::String fileName, bool isLinked, bool asIcon, std::basic_istream<CharType, Traits> &presentation)
```

## Se även

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertOleObject(System::String, System::String, bool, bool, std::basic_istream\<CharType, Traits\>\&) method




```cpp
template<typename CharType,typename Traits> System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOleObject(System::String fileName, System::String progId, bool isLinked, bool asIcon, std::basic_istream<CharType, Traits> &presentation)
```

## Se även

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
