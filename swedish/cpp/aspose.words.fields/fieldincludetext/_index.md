---
title: "Aspose::Words::Fields::FieldIncludeText klass"
linktitle: "FieldIncludeText"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::FieldIncludeText klass. Implementerar INCLUDETEXT-fältet. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 58000
url: /sv/cpp/aspose.words.fields/fieldincludetext/
---
## FieldIncludeText class


Implementerar INCLUDETEXT-fältet. För att lära dig mer, besök dokumentationsartikeln [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class FieldIncludeText : public Aspose::Words::Fields::Field,
                         public Aspose::Words::Fields::IFieldCodeTokenInfoProvider,
                         public Aspose::Words::Fields::IFieldIncludeTextCode
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [get_BookmarkName](./get_bookmarkname/)() override | Hämtar namnet på bokmärket i dokumentet som ska inkluderas. |
| [get_DisplayResult](../field/get_displayresult/)() | Hämtar texten som representerar det visade fältresultatet. |
| [get_Encoding](./get_encoding/)() | Hämtar kodningen som tillämpas på data i den refererade filen. |
| [get_End](../field/get_end/)() const | Hämtar noden som representerar fältets slut. |
| [get_FieldEnd](../field/get_fieldend/)() const | Hämtar noden som representerar fältets slut. |
| [get_FieldStart](../field/get_fieldstart/)() const | Hämtar noden som representerar fältets början. |
| [get_Format](../field/get_format/)() | Hämtar ett [FieldFormat](../fieldformat/) objekt som ger typad åtkomst till fältets formatering. |
| [get_IsDirty](../field/get_isdirty/)() | Hämtar eller anger om det aktuella resultatet av fältet inte längre är korrekt (föråldrat) på grund av andra ändringar som gjorts i dokumentet. |
| [get_IsLocked](../field/get_islocked/)() | Hämtar eller anger om fältet är låst (bör inte beräkna om sitt resultat). |
| [get_LocaleId](../field/get_localeid/)() | Hämtar eller anger LCID för fältet. |
| [get_LockFields](./get_lockfields/)() override | Hämtar om fält i det inkluderade dokumentet ska förhindras från att uppdateras. |
| [get_MimeType](./get_mimetype/)() | Hämtar MIME-typen för den refererade filen. |
| [get_NamespaceMappings](./get_namespacemappings/)() override | Hämtar namnrymdsmappningarna för XPath-frågor. |
| [get_Result](../field/get_result/)() | Hämtar eller anger text som ligger mellan fältavgränsaren och fältets slut. |
| [get_Separator](../field/get_separator/)() | Hämtar noden som representerar fältavgränsaren. Kan vara **null**. |
| [get_SourceFullName](./get_sourcefullname/)() override | Hämtar dokumentets plats med en IRI. |
| [get_Start](../field/get_start/)() const | Hämtar noden som representerar fältets början. |
| [get_TextConverter](./get_textconverter/)() override | Hämtar namnet på textkonverteraren för formatet på den inkluderade filen. |
| virtual [get_Type](../field/get_type/)() const | Hämtar Microsoft Word-fälttypen. |
| [get_XPath](./get_xpath/)() override | Hämtar XPath för den önskade delen av XML-filen. |
| [get_XslTransformation](./get_xsltransformation/)() override | Hämtar platsen för XSL-transformationen för att formatera XML-data. |
| [GetFieldCode](../field/getfieldcode/)() | Returnerar text mellan fältets början och fältavgränsaren (eller fältets slut om det inte finns någon avgränsare). Både fältkod och fältresultat för underfält inkluderas. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Returnerar text mellan fältets början och fältavgränsaren (eller fältets slut om det inte finns någon avgränsare). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Tar bort fältet från dokumentet. Returnerar en nod precis efter fältet. Om fältets slut är det sista barnet till dess föräldranod, returneras dess föräldrapparagraf. Om fältet redan har tagits bort, returneras **null**. |
| [set_BookmarkName](./set_bookmarkname/)(const System::String\&) | Ställer in namnet på bokmärket i dokumentet som ska inkluderas. |
| [set_Encoding](./set_encoding/)(const System::String\&) | Ställer in kodningen som tillämpas på data i den refererade filen. |
| [set_IsDirty](../field/set_isdirty/)(bool) | Sättare för [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Sättare för [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Sättare för [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_LockFields](./set_lockfields/)(bool) | Ställer in om fält i det inkluderade dokumentet ska förhindras att uppdateras. |
| [set_MimeType](./set_mimetype/)(const System::String\&) | Ställer in MIME-typen för den refererade filen. |
| [set_NamespaceMappings](./set_namespacemappings/)(const System::String\&) | Ställer in namnrymdsmappningarna för XPath‑frågor. |
| [set_Result](../field/set_result/)(const System::String\&) | Sättare för [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_SourceFullName](./set_sourcefullname/)(const System::String\&) | Ställer in dokumentets plats med en IRI. |
| [set_TextConverter](./set_textconverter/)(const System::String\&) | Ställer in namnet på textkonverteraren för formatet på den inkluderade filen. |
| [set_XPath](./set_xpath/)(const System::String\&) | Ställer in XPath för den önskade delen av XML‑filen. |
| [set_XslTransformation](./set_xsltransformation/)(const System::String\&) | Ställer in platsen för XSL‑transformering för att formatera XML‑data. |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Utför avlänkning av fältet. |
| [Update](../field/update/)() | Utför fältuppdateringen. Kastar ett undantag om fältet redan uppdateras. |
| [Update](../field/update/)(bool) | Utför en fältuppdatering. Kastar ett undantag om fältet redan uppdateras. |
## Se även

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
