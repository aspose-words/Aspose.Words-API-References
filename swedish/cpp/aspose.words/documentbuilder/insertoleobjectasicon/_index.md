---
title: "Aspose::Words::DocumentBuilder::InsertOleObjectAsIcon method"
linktitle: "InsertOleObjectAsIcon"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::DocumentBuilder::InsertOleObjectAsIcon method. Infogar ett inbäddat OLE-objekt som ikon från en ström till dokumentet. Tillåter att ange ikonfil och bildtext. Detekterar OLE-objektets typ med hjälp av den angivna progID‑parametern i C++."
type: docs
weight: 42000
url: /sv/cpp/aspose.words/documentbuilder/insertoleobjectasicon/
---
## DocumentBuilder::InsertOleObjectAsIcon(const System::SharedPtr\<System::IO::Stream\>\&, const System::String\&, const System::String\&, const System::String\&) method


Infogar ett inbäddat OLE-objekt som ikon från en ström i dokumentet. Tillåter att ange ikonfil och bildtext. Detekterar OLE-objekttyp med hjälp av angivet progID-parameter.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOleObjectAsIcon(const System::SharedPtr<System::IO::Stream> &stream, const System::String &progId, const System::String &iconFile, const System::String &iconCaption)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| ström | const System::SharedPtr\<System::IO::Stream\>\& | Ström som innehåller programdata. |
| progId | const System::String\& | ProgId för OLE-objekt. |
| iconFile | const System::String\& | Fullständig sökväg till ICO-filen. Om värdet är **null**, kommer Aspose.Words att använda en fördefinierad bild. |
| iconCaption | const System::String\& | Ikontext. Om värdet är **null**, kommer Aspose.Words att använda en fördefinierad ikontext. |

### ReturnValue

Formnod som innehåller Ole-objekt och infogas på den aktuella Builder‑positionen.

## Exempel



Visar hur man infogar ett inbäddat eller länkat OLE-objekt som ikon i dokumentet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Om 'iconFile' och 'iconCaption' utelämnas, väljer denna överlagrade metod
// ikonen enligt 'progId' och använder filnamnet som ikontext.
builder->InsertOleObjectAsIcon(get_MyDir() + u"Presentation.pptx", u"Package", false, get_ImageDir() + u"Logo icon.ico", u"My embedded file");

builder->InsertBreak(Aspose::Words::BreakType::LineBreak);

{
    auto stream = System::MakeObject<System::IO::FileStream>(get_MyDir() + u"Presentation.pptx", System::IO::FileMode::Open);
    // Om 'iconFile' och 'iconCaption' utelämnas, väljer denna överlagrade metod
    // ikonen enligt filändelsen och använder filnamnet som ikontext.
    System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertOleObjectAsIcon(stream, u"PowerPoint.Application", get_ImageDir() + u"Logo icon.ico", u"My embedded file stream");

    System::SharedPtr<Aspose::Words::Drawing::OlePackage> setOlePackage = shape->get_OleFormat()->get_OlePackage();
    setOlePackage->set_FileName(u"Presentation.pptx");
    setOlePackage->set_DisplayName(u"Presentation.pptx");
}

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertOleObjectAsIcon.docx");
```

## Se även

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertOleObjectAsIcon(const System::String\&, bool, const System::String\&, const System::String\&) method


Infogar ett inbäddat eller länkat OLE-objekt som ikon i dokumentet. Tillåter att ange ikonfil och bildtext. Detekterar OLE-objekttyp med hjälp av filändelse.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOleObjectAsIcon(const System::String &fileName, bool isLinked, const System::String &iconFile, const System::String &iconCaption)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| fileName | const System::String\& | Fullständig sökväg till filen. |
| isLinked | bool | Om **true** så infogas ett länkat OLE-objekt, annars infogas ett inbäddat OLE-objekt. |
| iconFile | const System::String\& | Fullständig sökväg till ICO-filen. Om värdet är **null**, kommer Aspose.Words att använda en fördefinierad bild. |
| iconCaption | const System::String\& | Ikontext. Om värdet är **null**, kommer Aspose.Words att använda filnamnet. |

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
## DocumentBuilder::InsertOleObjectAsIcon(const System::String\&, const System::String\&, bool, const System::String\&, const System::String\&) method


Infogar ett inbäddat eller länkat OLE-objekt som ikon i dokumentet. Tillåter att ange ikonfil och bildtext. Detekterar OLE-objekttyp med hjälp av angivet progID-parameter.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOleObjectAsIcon(const System::String &fileName, const System::String &progId, bool isLinked, const System::String &iconFile, const System::String &iconCaption)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| fileName | const System::String\& | Fullständig sökväg till filen. |
| progId | const System::String\& | ProgId för OLE-objekt. |
| isLinked | bool | Om **true** så infogas ett länkat OLE-objekt, annars infogas ett inbäddat OLE-objekt. |
| iconFile | const System::String\& | Fullständig sökväg till ICO-filen. Om värdet är **null**, kommer Aspose.Words att använda en fördefinierad bild. |
| iconCaption | const System::String\& | Ikontext. Om värdet är **null**, kommer Aspose.Words att använda filnamnet. |

### ReturnValue

Formnod som innehåller Ole-objekt och infogas på den aktuella Builder‑positionen.

## Exempel



Visar hur man infogar ett inbäddat eller länkat OLE-objekt som ikon i dokumentet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Om 'iconFile' och 'iconCaption' utelämnas, väljer denna överlagrade metod
// ikonen enligt 'progId' och använder filnamnet som ikontext.
builder->InsertOleObjectAsIcon(get_MyDir() + u"Presentation.pptx", u"Package", false, get_ImageDir() + u"Logo icon.ico", u"My embedded file");

builder->InsertBreak(Aspose::Words::BreakType::LineBreak);

{
    auto stream = System::MakeObject<System::IO::FileStream>(get_MyDir() + u"Presentation.pptx", System::IO::FileMode::Open);
    // Om 'iconFile' och 'iconCaption' utelämnas, väljer denna överlagrade metod
    // ikonen enligt filändelsen och använder filnamnet som ikontext.
    System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertOleObjectAsIcon(stream, u"PowerPoint.Application", get_ImageDir() + u"Logo icon.ico", u"My embedded file stream");

    System::SharedPtr<Aspose::Words::Drawing::OlePackage> setOlePackage = shape->get_OleFormat()->get_OlePackage();
    setOlePackage->set_FileName(u"Presentation.pptx");
    setOlePackage->set_DisplayName(u"Presentation.pptx");
}

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertOleObjectAsIcon.docx");
```

## Se även

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertOleObjectAsIcon(std::basic_istream\<CharType, Traits\>\&, System::String, System::String, System::String) method




```cpp
template<typename CharType,typename Traits> System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOleObjectAsIcon(std::basic_istream<CharType, Traits> &stream, System::String progId, System::String iconFile, System::String iconCaption)
```

## Se även

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
