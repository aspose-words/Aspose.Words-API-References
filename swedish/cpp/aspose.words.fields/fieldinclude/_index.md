---
title: "Aspose::Words::Fields::FieldInclude klass"
linktitle: "FieldInclude"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::FieldInclude klass. Implementerar INCLUDE‑fältet. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 56000
url: /sv/cpp/aspose.words.fields/fieldinclude/
---
## FieldInclude class


Implementerar INCLUDE-fältet. För att lära dig mer, besök dokumentationsartikeln [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class FieldInclude : public Aspose::Words::Fields::Field,
                     public Aspose::Words::Fields::IFieldCodeTokenInfoProvider,
                     public Aspose::Words::Fields::IFieldIncludeTextCode
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [get_BookmarkName](./get_bookmarkname/)() override | Hämtar eller anger namnet på bokmärket i dokumentet som ska inkluderas. |
| [get_DisplayResult](../field/get_displayresult/)() | Hämtar texten som representerar det visade fältresultatet. |
| [get_End](../field/get_end/)() const | Hämtar noden som representerar fältets slut. |
| [get_FieldEnd](../field/get_fieldend/)() const | Hämtar noden som representerar fältets slut. |
| [get_FieldStart](../field/get_fieldstart/)() const | Hämtar noden som representerar fältets början. |
| [get_Format](../field/get_format/)() | Hämtar ett [FieldFormat](../fieldformat/) objekt som ger typad åtkomst till fältets formatering. |
| [get_IsDirty](../field/get_isdirty/)() | Hämtar eller anger om det aktuella resultatet av fältet inte längre är korrekt (föråldrat) på grund av andra ändringar som gjorts i dokumentet. |
| [get_IsLocked](../field/get_islocked/)() | Hämtar eller anger om fältet är låst (bör inte beräkna om sitt resultat). |
| [get_LocaleId](../field/get_localeid/)() | Hämtar eller anger LCID för fältet. |
| [get_LockFields](./get_lockfields/)() override | Hämtar eller anger om fält i det inkluderade dokumentet ska förhindras från att uppdateras. |
| [get_Result](../field/get_result/)() | Hämtar eller anger text som ligger mellan fältavgränsaren och fältets slut. |
| [get_Separator](../field/get_separator/)() | Hämtar noden som representerar fältavgränsaren. Kan vara **null**. |
| [get_SourceFullName](./get_sourcefullname/)() override | Hämtar eller anger dokumentets plats. |
| [get_Start](../field/get_start/)() const | Hämtar noden som representerar fältets början. |
| [get_TextConverter](./get_textconverter/)() override | Hämtar eller anger namnet på textkonverteraren för formatet på den inkluderade filen. |
| virtual [get_Type](../field/get_type/)() const | Hämtar Microsoft Word-fälttypen. |
| [GetFieldCode](../field/getfieldcode/)() | Returnerar text mellan fältets början och fältavgränsaren (eller fältets slut om det inte finns någon avgränsare). Både fältkod och fältresultat för underfält inkluderas. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Returnerar text mellan fältets början och fältavgränsaren (eller fältets slut om det inte finns någon avgränsare). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Tar bort fältet från dokumentet. Returnerar en nod precis efter fältet. Om fältets slut är det sista barnet till dess föräldranod, returneras dess föräldrapparagraf. Om fältet redan har tagits bort, returneras **null**. |
| [set_BookmarkName](./set_bookmarkname/)(const System::String\&) | Sättare för [Aspose::Words::Fields::FieldInclude::get_BookmarkName](./get_bookmarkname/). |
| [set_IsDirty](../field/set_isdirty/)(bool) | Sättare för [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Sättare för [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Sättare för [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_LockFields](./set_lockfields/)(bool) | Sättare för [Aspose::Words::Fields::FieldInclude::get_LockFields](./get_lockfields/). |
| [set_Result](../field/set_result/)(const System::String\&) | Sättare för [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_SourceFullName](./set_sourcefullname/)(const System::String\&) | Sättare för [Aspose::Words::Fields::FieldInclude::get_SourceFullName](./get_sourcefullname/). |
| [set_TextConverter](./set_textconverter/)(const System::String\&) | Sättare för [Aspose::Words::Fields::FieldInclude::get_TextConverter](./get_textconverter/). |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Utför avlänkning av fältet. |
| [Update](../field/update/)() | Utför fältuppdateringen. Kastar ett undantag om fältet redan uppdateras. |
| [Update](../field/update/)(bool) | Utför en fältuppdatering. Kastar ett undantag om fältet redan uppdateras. |

## Exempel



Visar hur man skapar ett INCLUDE‑fält och sätter dess egenskaper.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Vi kan använda ett INCLUDE‑fält för att importera en del av ett annat dokument i det lokala filsystemet.
// Bokmärket från det andra dokumentet som vi refererar till med detta fält innehåller den importerade delen.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldInclude>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldInclude, true));
field->set_SourceFullName(get_MyDir() + u"Bookmarks.docx");
field->set_BookmarkName(u"MyBookmark1");
field->set_LockFields(false);
field->set_TextConverter(u"Microsoft Word");

ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(field->GetFieldCode(), u" INCLUDE .* MyBookmark1 \\\\c \"Microsoft Word\"")->get_Success());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.INCLUDE.docx");
```

## Se även

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
