---
title: "Aspose::Words::Fields::FieldDisplayBarcode-klass"
linktitle: "FieldDisplayBarcode"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::FieldDisplayBarcode-klass. Implementerar DISPLAYBARCODE-fältet. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 34000
url: /sv/cpp/aspose.words.fields/fielddisplaybarcode/
---
## FieldDisplayBarcode class


Implementerar DISPLAYBARCODE-fältet. För att lära dig mer, besök [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) dokumentationsartikel.

```cpp
class FieldDisplayBarcode : public Aspose::Words::Fields::Field,
                            public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [get_AddStartStopChar](./get_addstartstopchar/)() | Hämtar eller anger om Start/Stop-tecken ska läggas till för streckkodstyperna NW7 och CODE39. |
| [get_BackgroundColor](./get_backgroundcolor/)() | Hämtar eller anger bakgrundsfärgen för streckkodssymbolen. Giltiga värden ligger i intervallet [0, 0xFFFFFF]. |
| [get_BarcodeType](./get_barcodetype/)() | Hämtar eller anger streckkodstypen (QR, osv.) |
| [get_BarcodeValue](./get_barcodevalue/)() | Hämtar eller anger streckkodsvärdet. |
| [get_CaseCodeStyle](./get_casecodestyle/)() | Gets or sets the style of a Case Code for barcode type ITF14. The valid values are [STD | EXT | ADD]. |
| [get_DisplayResult](../field/get_displayresult/)() | Hämtar texten som representerar det visade fältresultatet. |
| [get_DisplayText](./get_displaytext/)() | Hämtar eller anger om streckkodsdata (text) ska visas tillsammans med bilden. |
| [get_End](../field/get_end/)() const | Hämtar noden som representerar fältets slut. |
| [get_ErrorCorrectionLevel](./get_errorcorrectionlevel/)() | Hämtar eller anger en felkorrigeringsnivå för QR‑kod. Giltiga värden är [0, 3]. |
| [get_FieldEnd](../field/get_fieldend/)() const | Hämtar noden som representerar fältets slut. |
| [get_FieldStart](../field/get_fieldstart/)() const | Hämtar noden som representerar fältets början. |
| [get_FixCheckDigit](./get_fixcheckdigit/)() | Hämtar eller anger om kontrollsiffran ska korrigeras om den är ogiltig. |
| [get_ForegroundColor](./get_foregroundcolor/)() | Hämtar eller anger förgrundsfärgen för streckkodssymbolen. Giltiga värden ligger i intervallet [0, 0xFFFFFF]. |
| [get_Format](../field/get_format/)() | Hämtar ett [FieldFormat](../fieldformat/) objekt som ger typad åtkomst till fältets formatering. |
| [get_IsDirty](../field/get_isdirty/)() | Hämtar eller anger om det aktuella resultatet av fältet inte längre är korrekt (föråldrat) på grund av andra ändringar som gjorts i dokumentet. |
| [get_IsLocked](../field/get_islocked/)() | Hämtar eller anger om fältet är låst (bör inte beräkna om sitt resultat). |
| [get_LocaleId](../field/get_localeid/)() | Hämtar eller anger LCID för fältet. |
| [get_PosCodeStyle](./get_poscodestyle/)() | Gets or sets the style of a Point of Sale barcode (barcode types UPCA | UPCE | EAN13 | EAN8). The valid values (case insensitive) are [STD | SUP2 | SUP5 | CASE]. |
| [get_Result](../field/get_result/)() | Hämtar eller anger text som ligger mellan fältavgränsaren och fältets slut. |
| [get_ScalingFactor](./get_scalingfactor/)() | Hämtar eller anger en skalningsfaktor för symbolen. Värdet är i hela procentenheter och giltiga värden är [10, 1000]. |
| [get_Separator](../field/get_separator/)() | Hämtar noden som representerar fältavgränsaren. Kan vara **null**. |
| [get_Start](../field/get_start/)() const | Hämtar noden som representerar fältets början. |
| [get_SymbolHeight](./get_symbolheight/)() | Hämtar eller anger symbolens höjd. Enheterna är i TWIPS (1/1440 tum). |
| [get_SymbolRotation](./get_symbolrotation/)() | Hämtar eller anger rotationen för streckkodssymbolen. Giltiga värden är [0, 3]. |
| virtual [get_Type](../field/get_type/)() const | Hämtar Microsoft Word-fälttypen. |
| [GetFieldCode](../field/getfieldcode/)() | Returnerar text mellan fältets början och fältavgränsaren (eller fältets slut om det inte finns någon avgränsare). Både fältkod och fältresultat för underfält inkluderas. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Returnerar text mellan fältets början och fältavgränsaren (eller fältets slut om det inte finns någon avgränsare). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Tar bort fältet från dokumentet. Returnerar en nod precis efter fältet. Om fältets slut är det sista barnet till dess föräldranod, returneras dess föräldrapparagraf. Om fältet redan har tagits bort, returneras **null**. |
| [set_AddStartStopChar](./set_addstartstopchar/)(bool) | Sättare för [Aspose::Words::Fields::FieldDisplayBarcode::get_AddStartStopChar](./get_addstartstopchar/). |
| [set_BackgroundColor](./set_backgroundcolor/)(const System::String\&) | Sättare för [Aspose::Words::Fields::FieldDisplayBarcode::get_BackgroundColor](./get_backgroundcolor/). |
| [set_BarcodeType](./set_barcodetype/)(const System::String\&) | Sättare för [Aspose::Words::Fields::FieldDisplayBarcode::get_BarcodeType](./get_barcodetype/). |
| [set_BarcodeValue](./set_barcodevalue/)(const System::String\&) | Sättare för [Aspose::Words::Fields::FieldDisplayBarcode::get_BarcodeValue](./get_barcodevalue/). |
| [set_CaseCodeStyle](./set_casecodestyle/)(const System::String\&) | Sättare för [Aspose::Words::Fields::FieldDisplayBarcode::get_CaseCodeStyle](./get_casecodestyle/). |
| [set_DisplayText](./set_displaytext/)(bool) | Sättare för [Aspose::Words::Fields::FieldDisplayBarcode::get_DisplayText](./get_displaytext/). |
| [set_ErrorCorrectionLevel](./set_errorcorrectionlevel/)(const System::String\&) | Sättare för [Aspose::Words::Fields::FieldDisplayBarcode::get_ErrorCorrectionLevel](./get_errorcorrectionlevel/). |
| [set_FixCheckDigit](./set_fixcheckdigit/)(bool) | Sättare för [Aspose::Words::Fields::FieldDisplayBarcode::get_FixCheckDigit](./get_fixcheckdigit/). |
| [set_ForegroundColor](./set_foregroundcolor/)(const System::String\&) | Sättare för [Aspose::Words::Fields::FieldDisplayBarcode::get_ForegroundColor](./get_foregroundcolor/). |
| [set_IsDirty](../field/set_isdirty/)(bool) | Sättare för [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Sättare för [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Sättare för [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_PosCodeStyle](./set_poscodestyle/)(const System::String\&) | Sättare för [Aspose::Words::Fields::FieldDisplayBarcode::get_PosCodeStyle](./get_poscodestyle/). |
| [set_Result](../field/set_result/)(const System::String\&) | Sättare för [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_ScalingFactor](./set_scalingfactor/)(const System::String\&) | Sättare för [Aspose::Words::Fields::FieldDisplayBarcode::get_ScalingFactor](./get_scalingfactor/). |
| [set_SymbolHeight](./set_symbolheight/)(const System::String\&) | Sättare för [Aspose::Words::Fields::FieldDisplayBarcode::get_SymbolHeight](./get_symbolheight/). |
| [set_SymbolRotation](./set_symbolrotation/)(const System::String\&) | Sättare för [Aspose::Words::Fields::FieldDisplayBarcode::get_SymbolRotation](./get_symbolrotation/). |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Utför avlänkning av fältet. |
| [Update](../field/update/)() | Utför fältuppdateringen. Kastar ett undantag om fältet redan uppdateras. |
| [Update](../field/update/)(bool) | Utför en fältuppdatering. Kastar ett undantag om fältet redan uppdateras. |

## Exempel



Visar hur man infogar ett DISPLAYBARCODE-fält och anger dess egenskaper.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto field = System::ExplicitCast<Aspose::Words::Fields::FieldDisplayBarcode>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDisplayBarcode, true));

// Nedan finns fyra typer av streckkoder, dekorerade på olika sätt, som DISPLAYBARCODE-fältet kan visa.
// 1 -  QR-kod med anpassade färger:
field->set_BarcodeType(u"QR");
field->set_BarcodeValue(u"ABC123");
field->set_BackgroundColor(u"0xF8BD69");
field->set_ForegroundColor(u"0xB5413B");
field->set_ErrorCorrectionLevel(u"3");
field->set_ScalingFactor(u"250");
field->set_SymbolHeight(u"1000");
field->set_SymbolRotation(u"0");

ASSERT_EQ(u" DISPLAYBARCODE  ABC123 QR \\b 0xF8BD69 \\f 0xB5413B \\q 3 \\s 250 \\h 1000 \\r 0", field->GetFieldCode());
builder->Writeln();

// 2 -  EAN13-streckkod, med siffrorna visade under staplarna:
field = System::ExplicitCast<Aspose::Words::Fields::FieldDisplayBarcode>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDisplayBarcode, true));
field->set_BarcodeType(u"EAN13");
field->set_BarcodeValue(u"501234567890");
field->set_DisplayText(true);
field->set_PosCodeStyle(u"CASE");
field->set_FixCheckDigit(true);

ASSERT_EQ(u" DISPLAYBARCODE  501234567890 EAN13 \\t \\p CASE \\x", field->GetFieldCode());
builder->Writeln();

// 3 -  CODE39-streckkod:
field = System::ExplicitCast<Aspose::Words::Fields::FieldDisplayBarcode>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDisplayBarcode, true));
field->set_BarcodeType(u"CODE39");
field->set_BarcodeValue(u"12345ABCDE");
field->set_AddStartStopChar(true);

ASSERT_EQ(u" DISPLAYBARCODE  12345ABCDE CODE39 \\d", field->GetFieldCode());
builder->Writeln();

// 4 -  ITF4-streckkod, med en specificerad case-kod:
field = System::ExplicitCast<Aspose::Words::Fields::FieldDisplayBarcode>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDisplayBarcode, true));
field->set_BarcodeType(u"ITF14");
field->set_BarcodeValue(u"09312345678907");
field->set_CaseCodeStyle(u"STD");

ASSERT_EQ(u" DISPLAYBARCODE  09312345678907 ITF14 \\c STD", field->GetFieldCode());

doc->Save(get_ArtifactsDir() + u"Field.DISPLAYBARCODE.docx");
```

## Se även

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
