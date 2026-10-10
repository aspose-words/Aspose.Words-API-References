---
title: "Aspose::Words::Fields::FieldRef class"
linktitle: "FieldRef"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::FieldRef class. Implementerar REF-fältet. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 85000
url: /sv/cpp/aspose.words.fields/fieldref/
---
## FieldRef class


Implementerar REF-fältet. För att lära dig mer, besök dokumentationsartikeln [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class FieldRef : public Aspose::Words::Fields::Field,
                 public Aspose::Words::Fields::IFieldCodeTokenInfoProvider,
                 public Aspose::Words::Fields::IMergeFieldSurrogate
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [get_BookmarkName](./get_bookmarkname/)() | Hämtar eller anger namnet på den refererade bokmärket. |
| [get_DisplayResult](../field/get_displayresult/)() | Hämtar texten som representerar det visade fältresultatet. |
| [get_End](./get_end/)() override | Hämtar noden som representerar fältets slut. |
| [get_End](../field/get_end/)() const | Hämtar noden som representerar fältets slut. |
| [get_FieldEnd](../field/get_fieldend/)() const | Hämtar noden som representerar fältets slut. |
| [get_FieldStart](../field/get_fieldstart/)() const | Hämtar noden som representerar fältets början. |
| [get_Format](../field/get_format/)() | Hämtar ett [FieldFormat](../fieldformat/) objekt som ger typad åtkomst till fältets formatering. |
| [get_IncludeNoteOrComment](./get_includenoteorcomment/)() | Hämtar om fotnot-, slutnot- och annoteringsnummer som markerats av bokmärket ska ökas, och infogar motsvarande fotnot-, slutnot- och kommentartext. |
| [get_InsertHyperlink](./get_inserthyperlink/)() | Hämtar om en hyperlänk till det bokmärkta stycket ska skapas. |
| [get_InsertParagraphNumber](./get_insertparagraphnumber/)() | Hämtar om styckesnumret för det refererade stycket ska infogas exakt som det visas i dokumentet. |
| [get_InsertParagraphNumberInFullContext](./get_insertparagraphnumberinfullcontext/)() | Hämtar om styckesnumret för det refererade stycket ska infogas i full kontext. |
| [get_InsertParagraphNumberInRelativeContext](./get_insertparagraphnumberinrelativecontext/)() | Hämtar om styckesnumret för det refererade stycket ska infogas i relativ kontext. |
| [get_InsertRelativePosition](./get_insertrelativeposition/)() | Hämtar om den relativa positionen för det refererade stycket ska infogas. |
| [get_IsDirty](../field/get_isdirty/)() | Hämtar eller anger om det aktuella resultatet av fältet inte längre är korrekt (föråldrat) på grund av andra ändringar som gjorts i dokumentet. |
| [get_IsLocked](../field/get_islocked/)() | Hämtar eller anger om fältet är låst (bör inte beräkna om sitt resultat). |
| [get_LocaleId](../field/get_localeid/)() | Hämtar eller anger LCID för fältet. |
| [get_NumberSeparator](./get_numberseparator/)() | Hämtar teckensekvensen som används för att separera sekvensnummer och sidnummer. |
| [get_Result](../field/get_result/)() | Hämtar eller anger text som ligger mellan fältavgränsaren och fältets slut. |
| [get_Separator](./get_separator/)() override | Hämtar noden som representerar fältavgränsaren. Kan vara **null**. |
| [get_Start](./get_start/)() override | Hämtar noden som representerar fältets början. |
| [get_Start](../field/get_start/)() const | Hämtar noden som representerar fältets början. |
| [get_SuppressNonDelimiters](./get_suppressnondelimiters/)() | Hämtar om icke-avgränsartecken ska undertryckas. |
| virtual [get_Type](../field/get_type/)() const | Hämtar Microsoft Word-fälttypen. |
| [GetFieldCode](../field/getfieldcode/)() | Returnerar text mellan fältets början och fältavgränsaren (eller fältets slut om det inte finns någon avgränsare). Både fältkod och fältresultat för underfält inkluderas. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Returnerar text mellan fältets början och fältavgränsaren (eller fältets slut om det inte finns någon avgränsare). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Tar bort fältet från dokumentet. Returnerar en nod precis efter fältet. Om fältets slut är det sista barnet till dess föräldranod, returneras dess föräldrapparagraf. Om fältet redan har tagits bort, returneras **null**. |
| [set_BookmarkName](./set_bookmarkname/)(const System::String\&) | Sättare för [Aspose::Words::Fields::FieldRef::get_BookmarkName](./get_bookmarkname/). |
| [set_IncludeNoteOrComment](./set_includenoteorcomment/)(bool) | Ställer in om fotnot-, slutnot- och annoteringsnummer som markeras av bokmärket ska ökas, och infoga motsvarande fotnot-, slutnot- och kommentarstext. |
| [set_InsertHyperlink](./set_inserthyperlink/)(bool) | Ställer in om en hyperlänk till det bokmärkta stycket ska skapas. |
| [set_InsertParagraphNumber](./set_insertparagraphnumber/)(bool) | Ställer in om styckesnumret för det refererade stycket ska infogas exakt som det visas i dokumentet. |
| [set_InsertParagraphNumberInFullContext](./set_insertparagraphnumberinfullcontext/)(bool) | Ställer in om styckesnumret för det refererade stycket ska infogas i full kontext. |
| [set_InsertParagraphNumberInRelativeContext](./set_insertparagraphnumberinrelativecontext/)(bool) | Ställer in om styckesnumret för det refererade stycket ska infogas i relativ kontext. |
| [set_InsertRelativePosition](./set_insertrelativeposition/)(bool) | Ställer in om den relativa positionen för det refererade stycket ska infogas. |
| [set_IsDirty](../field/set_isdirty/)(bool) | Sättare för [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Sättare för [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Sättare för [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_NumberSeparator](./set_numberseparator/)(const System::String\&) | Anger teckensekvensen som används för att separera sekvensnummer och sidnummer. |
| [set_Result](../field/set_result/)(const System::String\&) | Sättare för [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_SuppressNonDelimiters](./set_suppressnondelimiters/)(bool) | Ställer in om icke-avgränsande tecken ska undertryckas. |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Utför avlänkning av fältet. |
| [Update](../field/update/)() | Utför fältuppdateringen. Kastar ett undantag om fältet redan uppdateras. |
| [Update](../field/update/)(bool) | Utför en fältuppdatering. Kastar ett undantag om fältet redan uppdateras. |

## Exempel



Visar hur man skapar bokmärkt text med ett SET-fält, och sedan visar den i dokumentet med ett REF-fält.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Namnge bokmärkt text med ett SET-fält.
// Detta fält refererar till "bookmark" och inte en bokmärkesstruktur som visas i texten, utan en namngiven variabel.
auto fieldSet = System::ExplicitCast<Aspose::Words::Fields::FieldSet>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSet, false));
fieldSet->set_BookmarkName(u"MyBookmark");
fieldSet->set_BookmarkText(u"Hello world!");
fieldSet->Update();

ASSERT_EQ(u" SET  MyBookmark \"Hello world!\"", fieldSet->GetFieldCode());

// Referera till bokmärket med namn i ett REF-fält och visa dess innehåll.
auto fieldRef = System::ExplicitCast<Aspose::Words::Fields::FieldRef>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldRef, true));
fieldRef->set_BookmarkName(u"MyBookmark");
fieldRef->Update();

ASSERT_EQ(u" REF  MyBookmark", fieldRef->GetFieldCode());
ASSERT_EQ(u"Hello world!", fieldRef->get_Result());

doc->Save(get_ArtifactsDir() + u"Field.SET.REF.docx");
```

## Se även

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
