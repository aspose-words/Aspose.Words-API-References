---
title: "Aspose::Words::Drawing::OleFormat::Save method"
linktitle: "Spara"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::OleFormat::Save method. Sparar data för det inbäddade objektet i den angivna strömmen i C++."
type: docs
weight: 19000
url: /sv/cpp/aspose.words.drawing/oleformat/save/
---
## OleFormat::Save(const System::SharedPtr\<System::IO::Stream\>\&) method


Sparar data för det inbäddade objektet i den angivna strömmen.

```cpp
void Aspose::Words::Drawing::OleFormat::Save(const System::SharedPtr<System::IO::Stream> &stream)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| ström | const System::SharedPtr\<System::IO::Stream\>\& | Var man sparar objektdata. |
## Anmärkningar


Det är anroparens ansvar att avyttra strömmen.

## Exempel



Visar hur man extraherar inbäddade OLE-objekt till filer.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"OLE spreadsheet.docm");
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

// OLE-objektet i den första formen är ett Microsoft Excel-kalkylblad.
System::SharedPtr<Aspose::Words::Drawing::OleFormat> oleFormat = shape->get_OleFormat();

ASSERT_EQ(u"Excel.Sheet.12", oleFormat->get_ProgId());

// Vårt objekt uppdateras varken automatiskt eller är låst för uppdateringar.
ASSERT_FALSE(oleFormat->get_AutoUpdate());
ASPOSE_ASSERT_EQ(false, oleFormat->get_IsLocked());

// Om vi planerar att spara OLE-objektet till en fil i det lokala filsystemet,
// kan vi använda egenskapen "SuggestedExtension" för att bestämma vilken filändelse som ska tillämpas på filen.
ASSERT_EQ(u".xlsx", oleFormat->get_SuggestedExtension());

// Nedan följer två sätt att spara ett OLE-objekt till en fil i det lokala filsystemet.
// 1 -  Spara det via en ström:
{
    auto fs = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + u"OLE spreadsheet extracted via stream" + oleFormat->get_SuggestedExtension(), System::IO::FileMode::Create);
    oleFormat->Save(fs);
}

// 2 -  Spara det direkt till ett filnamn:
oleFormat->Save(get_ArtifactsDir() + u"OLE spreadsheet saved directly" + oleFormat->get_SuggestedExtension());
```

## Se även

* Class [OleFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
## OleFormat::Save(const System::String\&) method


Sparar data för det inbäddade objektet i en fil med det angivna namnet.

```cpp
void Aspose::Words::Drawing::OleFormat::Save(const System::String &fileName)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| fileName | const System::String\& | Namn på filen för att spara OLE-objektets data. |

## Exempel



Visar hur man extraherar inbäddade OLE-objekt till filer.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"OLE spreadsheet.docm");
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

// OLE-objektet i den första formen är ett Microsoft Excel-kalkylblad.
System::SharedPtr<Aspose::Words::Drawing::OleFormat> oleFormat = shape->get_OleFormat();

ASSERT_EQ(u"Excel.Sheet.12", oleFormat->get_ProgId());

// Vårt objekt uppdateras varken automatiskt eller är låst för uppdateringar.
ASSERT_FALSE(oleFormat->get_AutoUpdate());
ASPOSE_ASSERT_EQ(false, oleFormat->get_IsLocked());

// Om vi planerar att spara OLE-objektet till en fil i det lokala filsystemet,
// kan vi använda egenskapen "SuggestedExtension" för att bestämma vilken filändelse som ska tillämpas på filen.
ASSERT_EQ(u".xlsx", oleFormat->get_SuggestedExtension());

// Nedan följer två sätt att spara ett OLE-objekt till en fil i det lokala filsystemet.
// 1 -  Spara det via en ström:
{
    auto fs = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + u"OLE spreadsheet extracted via stream" + oleFormat->get_SuggestedExtension(), System::IO::FileMode::Create);
    oleFormat->Save(fs);
}

// 2 -  Spara det direkt till ett filnamn:
oleFormat->Save(get_ArtifactsDir() + u"OLE spreadsheet saved directly" + oleFormat->get_SuggestedExtension());
```

## Se även

* Class [OleFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
## OleFormat::Save(std::basic_ostream\<CharType, Traits\>\&) method




```cpp
template<typename CharType,typename Traits> void Aspose::Words::Drawing::OleFormat::Save(std::basic_ostream<CharType, Traits> &stream)
```

## Se även

* Class [OleFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
