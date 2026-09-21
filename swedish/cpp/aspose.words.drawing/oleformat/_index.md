---
title: "Aspose::Words::Drawing::OleFormat-klass"
linktitle: "OleFormat"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::OleFormat-klass. Tillhandahåller åtkomst till data för ett OLE-objekt eller en ActiveX-kontroll. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 8000
url: /sv/cpp/aspose.words.drawing/oleformat/
---
## OleFormat class


Ger åtkomst till data för ett OLE-objekt eller ActiveX‑kontroll. För att lära dig mer, besök dokumentationsartikeln [Working with Ole Objects](https://docs.aspose.com/words/cpp/working-with-ole-objects/).

```cpp
class OleFormat : public System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [get_AutoUpdate](./get_autoupdate/)() | Anger om länken till OLE-objektet automatiskt uppdateras eller inte i Microsoft Word. |
| [get_Clsid](./get_clsid/)() | Hämtar CLSID för OLE-objektet. |
| [get_IconCaption](./get_iconcaption/)() | Hämtar ikontext för OLE-objektet. Om OLE-objektet inte har en ikon eller om en text inte kan hämtas, returneras en tom sträng. |
| [get_IsLink](./get_islink/)() | Returnerar **true** om OLE-objektet är länkat (när [SourceFullName](./get_sourcefullname/) är angivet). |
| [get_IsLocked](./get_islocked/)() | Anger om länken till OLE-objektet är låst för uppdateringar. |
| [get_OleControl](./get_olecontrol/)() | Hämtar [OleControl](./get_olecontrol/)‑objekt om detta OLE-objekt är en ActiveX‑kontroll. Annars är denna egenskap null. |
| [get_OleIcon](./get_oleicon/)() | Hämtar ritningsaspekten för OLE-objektet. När **true** visas OLE-objektet som en ikon. När **false** visas OLE-objektet som innehåll. |
| [get_OlePackage](./get_olepackage/)() | Tillhandahåller åtkomst till [OlePackage](../olepackage/) om OLE-objektet är ett OLE‑paket. Returnerar **null** annars. |
| [get_ProgId](./get_progid/)() | Hämtar eller anger ProgID för OLE-objektet. |
| [get_SourceFullName](./get_sourcefullname/)() | Hämtar eller anger sökväg och namn för källfilen för det länkade OLE-objektet. |
| [get_SourceItem](./get_sourceitem/)() | Hämtar eller anger en sträng som används för att identifiera den del av källfilen som länkas. |
| [get_SuggestedExtension](./get_suggestedextension/)() | Hämtar filändelsen som föreslås för det aktuella inbäddade objektet om du vill spara det i en fil. |
| [get_SuggestedFileName](./get_suggestedfilename/)() | Hämtar filnamnet som föreslås för det aktuella inbäddade objektet om du vill spara det i en fil. |
| [GetOleEntry](./getoleentry/)(const System::String\&) | Hämtar OLE-objektets dataentry. |
| [GetRawData](./getrawdata/)() | Hämtar OLE-objektets rådata. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Save](./save/)(const System::SharedPtr\<System::IO::Stream\>\&) | Sparar data för det inbäddade objektet i den angivna strömmen. |
| [Save](./save/)(const System::String\&) | Sparar data för det inbäddade objektet i en fil med det angivna namnet. |
| [Save](./save/)(std::basic_ostream\<CharType, Traits\>\&) |  |
| [set_AutoUpdate](./set_autoupdate/)(bool) | Sättare för [Aspose::Words::Drawing::OleFormat::get_AutoUpdate](./get_autoupdate/). |
| [set_IsLocked](./set_islocked/)(bool) | Settern för [Aspose::Words::Drawing::OleFormat::get_IsLocked](./get_islocked/). |
| [set_ProgId](./set_progid/)(const System::String\&) | Settern för [Aspose::Words::Drawing::OleFormat::get_ProgId](./get_progid/). |
| [set_SourceFullName](./set_sourcefullname/)(const System::String\&) | Settern för [Aspose::Words::Drawing::OleFormat::get_SourceFullName](./get_sourcefullname/). |
| [set_SourceItem](./set_sourceitem/)(const System::String\&) | Settern för [Aspose::Words::Drawing::OleFormat::get_SourceItem](./get_sourceitem/). |
| static [Type](./type/)() |  |
## Anmärkningar


Använd egenskapen [OleFormat](../shape/get_oleformat/) för att komma åt data i ett OLE-objekt. Du skapar inte instanser av klassen [OleFormat](./) direkt.

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

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
