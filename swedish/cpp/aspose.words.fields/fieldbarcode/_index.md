---
title: "Aspose::Words::Fields::FieldBarcode class"
linktitle: "FieldBarcode"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::FieldBarcode class. Implementerar BARCODE-fältet. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 17000
url: /sv/cpp/aspose.words.fields/fieldbarcode/
---
## FieldBarcode class


Implementerar BARCODE-fältet. För att lära dig mer, besök [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) dokumentationsartikel.

```cpp
class FieldBarcode : public Aspose::Words::Fields::Field,
                     public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [get_DisplayResult](../field/get_displayresult/)() | Hämtar texten som representerar det visade fältresultatet. |
| [get_End](../field/get_end/)() const | Hämtar noden som representerar fältets slut. |
| [get_FacingIdentificationMark](./get_facingidentificationmark/)() | Hämtar eller anger typen av ett Facing Identification Mark (FIM) att infoga. |
| [get_FieldEnd](../field/get_fieldend/)() const | Hämtar noden som representerar fältets slut. |
| [get_FieldStart](../field/get_fieldstart/)() const | Hämtar noden som representerar fältets början. |
| [get_Format](../field/get_format/)() | Hämtar ett [FieldFormat](../fieldformat/) objekt som ger typad åtkomst till fältets formatering. |
| [get_IsBookmark](./get_isbookmark/)() | Hämtar eller anger om [PostalAddress](./get_postaladdress/) är namnet på ett bokmärke. |
| [get_IsDirty](../field/get_isdirty/)() | Hämtar eller anger om det aktuella resultatet av fältet inte längre är korrekt (föråldrat) på grund av andra ändringar som gjorts i dokumentet. |
| [get_IsLocked](../field/get_islocked/)() | Hämtar eller anger om fältet är låst (bör inte beräkna om sitt resultat). |
| [get_IsUSPostalAddress](./get_isuspostaladdress/)() | Hämtar eller anger om [PostalAddress](./get_postaladdress/) är en amerikansk postadress. |
| [get_LocaleId](../field/get_localeid/)() | Hämtar eller anger LCID för fältet. |
| [get_PostalAddress](./get_postaladdress/)() | Hämtar eller anger postadressen som används för att generera en streckkod eller namnet på bokmärket som refererar till den. |
| [get_Result](../field/get_result/)() | Hämtar eller anger text som ligger mellan fältavgränsaren och fältets slut. |
| [get_Separator](../field/get_separator/)() | Hämtar noden som representerar fältavgränsaren. Kan vara **null**. |
| [get_Start](../field/get_start/)() const | Hämtar noden som representerar fältets början. |
| virtual [get_Type](../field/get_type/)() const | Hämtar Microsoft Word-fälttypen. |
| [GetFieldCode](../field/getfieldcode/)() | Returnerar text mellan fältets början och fältavgränsaren (eller fältets slut om det inte finns någon avgränsare). Både fältkod och fältresultat för underfält inkluderas. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Returnerar text mellan fältets början och fältavgränsaren (eller fältets slut om det inte finns någon avgränsare). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Tar bort fältet från dokumentet. Returnerar en nod precis efter fältet. Om fältets slut är det sista barnet till dess föräldranod, returneras dess föräldrapparagraf. Om fältet redan har tagits bort, returneras **null**. |
| [set_FacingIdentificationMark](./set_facingidentificationmark/)(const System::String\&) | Sättare för [Aspose::Words::Fields::FieldBarcode::get_FacingIdentificationMark](./get_facingidentificationmark/). |
| [set_IsBookmark](./set_isbookmark/)(bool) | Sättare för [Aspose::Words::Fields::FieldBarcode::get_IsBookmark](./get_isbookmark/). |
| [set_IsDirty](../field/set_isdirty/)(bool) | Sättare för [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Sättare för [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_IsUSPostalAddress](./set_isuspostaladdress/)(bool) | Sättare för [Aspose::Words::Fields::FieldBarcode::get_IsUSPostalAddress](./get_isuspostaladdress/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Sättare för [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_PostalAddress](./set_postaladdress/)(const System::String\&) | Sättare för [Aspose::Words::Fields::FieldBarcode::get_PostalAddress](./get_postaladdress/). |
| [set_Result](../field/set_result/)(const System::String\&) | Sättare för [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Utför avlänkning av fältet. |
| [Update](../field/update/)() | Utför fältuppdateringen. Kastar ett undantag om fältet redan uppdateras. |
| [Update](../field/update/)(bool) | Utför en fältuppdatering. Kastar ett undantag om fältet redan uppdateras. |

## Exempel



Visar hur man använder BARCODE-fältet för att visa amerikanska postnummer i form av en streckkod.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln();

// Nedan finns två sätt att använda BARCODE-fält för att visa anpassade värden som streckkoder.
// 1 -  Spara värdet som streckkoden ska visa i egenskapen PostalAddress:
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldBarcode>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldBarcode, true));

// Detta värde måste vara ett giltigt postnummer.
field->set_PostalAddress(u"96801");
field->set_IsUSPostalAddress(true);
field->set_FacingIdentificationMark(u"C");

ASSERT_EQ(u" BARCODE  96801 \\u \\f C", field->GetFieldCode());

builder->InsertBreak(Aspose::Words::BreakType::LineBreak);

// 2 -  Referera till ett bokmärke som lagrar värdet som denna streckkod ska visa:
field = System::ExplicitCast<Aspose::Words::Fields::FieldBarcode>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldBarcode, true));
field->set_PostalAddress(u"BarcodeBookmark");
field->set_IsBookmark(true);

ASSERT_EQ(u" BARCODE  BarcodeBookmark \\b", field->GetFieldCode());

// Bokmärket som BARCODE-fältet refererar till i sin egenskap PostalAddress
// måste bara innehålla det giltiga postnumret.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->StartBookmark(u"BarcodeBookmark");
builder->Writeln(u"968877");
builder->EndBookmark(u"BarcodeBookmark");

doc->Save(get_ArtifactsDir() + u"Field.BARCODE.docx");
```

## Se även

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
