---
title: "Aspose::Words::Fields::FieldNoteRef klass"
linktitle: "FieldNoteRef"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::FieldNoteRef klass. Implementerar NOTEREF-fältet. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 72000
url: /sv/cpp/aspose.words.fields/fieldnoteref/
---
## FieldNoteRef class


Implementerar NOTEREF-fältet. För att lära dig mer, besök dokumentationsartikeln [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class FieldNoteRef : public Aspose::Words::Fields::Field,
                     public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [get_BookmarkName](./get_bookmarkname/)() | Hämtar namnet på bokmärket. |
| [get_DisplayResult](../field/get_displayresult/)() | Hämtar texten som representerar det visade fältresultatet. |
| [get_End](../field/get_end/)() const | Hämtar noden som representerar fältets slut. |
| [get_FieldEnd](../field/get_fieldend/)() const | Hämtar noden som representerar fältets slut. |
| [get_FieldStart](../field/get_fieldstart/)() const | Hämtar noden som representerar fältets början. |
| [get_Format](../field/get_format/)() | Hämtar ett [FieldFormat](../fieldformat/) objekt som ger typad åtkomst till fältets formatering. |
| [get_InsertHyperlink](./get_inserthyperlink/)() | Hämtar om en hyperlänk ska infogas till det bokmärkta stycket. |
| [get_InsertReferenceMark](./get_insertreferencemark/)() | Infogar referensmärket med samma teckenformatering som stilen för fotnotreferens eller slutnotreferens. |
| [get_InsertRelativePosition](./get_insertrelativeposition/)() | Hämtar om en relativ position för det bokmärkta stycket ska infogas. |
| [get_IsDirty](../field/get_isdirty/)() | Hämtar eller anger om det aktuella resultatet av fältet inte längre är korrekt (föråldrat) på grund av andra ändringar som gjorts i dokumentet. |
| [get_IsLocked](../field/get_islocked/)() | Hämtar eller anger om fältet är låst (bör inte beräkna om sitt resultat). |
| [get_LocaleId](../field/get_localeid/)() | Hämtar eller anger LCID för fältet. |
| [get_Result](../field/get_result/)() | Hämtar eller anger text som ligger mellan fältavgränsaren och fältets slut. |
| [get_Separator](../field/get_separator/)() | Hämtar noden som representerar fältavgränsaren. Kan vara **null**. |
| [get_Start](../field/get_start/)() const | Hämtar noden som representerar fältets början. |
| virtual [get_Type](../field/get_type/)() const | Hämtar Microsoft Word-fälttypen. |
| [GetFieldCode](../field/getfieldcode/)() | Returnerar text mellan fältets början och fältavgränsaren (eller fältets slut om det inte finns någon avgränsare). Både fältkod och fältresultat för underfält inkluderas. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Returnerar text mellan fältets början och fältavgränsaren (eller fältets slut om det inte finns någon avgränsare). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Tar bort fältet från dokumentet. Returnerar en nod precis efter fältet. Om fältets slut är det sista barnet till dess föräldranod, returneras dess föräldrapparagraf. Om fältet redan har tagits bort, returneras **null**. |
| [set_BookmarkName](./set_bookmarkname/)(const System::String\&) | Ställer in namnet på bokmärket. |
| [set_InsertHyperlink](./set_inserthyperlink/)(bool) | Anger om en hyperlänk till det bokmärkta stycket ska infogas. |
| [set_InsertReferenceMark](./set_insertreferencemark/)(bool) | Infogar referensmärket med samma teckenformatering som stilen för fotnotreferens eller slutnotreferens. |
| [set_InsertRelativePosition](./set_insertrelativeposition/)(bool) | Anger om en relativ position för det bokmärkta stycket ska infogas. |
| [set_IsDirty](../field/set_isdirty/)(bool) | Sättare för [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Sättare för [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Sättare för [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_Result](../field/set_result/)(const System::String\&) | Sättare för [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Utför avlänkning av fältet. |
| [Update](../field/update/)() | Utför fältuppdateringen. Kastar ett undantag om fältet redan uppdateras. |
| [Update](../field/update/)(bool) | Utför en fältuppdatering. Kastar ett undantag om fältet redan uppdateras. |

## Exempel



Visar hur man korsrefererar fotnoter med NOTEREF-fältet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"CrossReference: ");

auto field = System::ExplicitCast<Aspose::Words::Fields::FieldNoteRef>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldNoteRef, false));
// <--- uppdatera inte fältet
field->set_BookmarkName(u"CrossRefBookmark");
field->set_InsertHyperlink(true);
field->set_InsertReferenceMark(true);
field->set_InsertRelativePosition(false);
builder->Writeln();

builder->StartBookmark(u"CrossRefBookmark");
builder->Write(u"Hello world!");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Cross referenced footnote.");
builder->EndBookmark(u"CrossRefBookmark");
builder->Writeln();

doc->UpdateFields();

// Detta fält fungerar endast i äldre versioner av Microsoft Word.
doc->Save(get_ArtifactsDir() + u"Field.NOTEREF.doc");
```

## Se även

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
