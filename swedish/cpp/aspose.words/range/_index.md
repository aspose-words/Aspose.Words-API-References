---
title: "Aspose::Words::Range-klass"
linktitle: "Område"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Range-klass. Representerar ett sammanhängande område i ett dokument. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 51000
url: /sv/cpp/aspose.words/range/
---
## Range class


Representerar ett sammanhängande område i ett dokument. För att lära dig mer, besök dokumentationsartikeln [Working with Ranges](https://docs.aspose.com/words/cpp/working-with-ranges/).

```cpp
class Range : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Node>>
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [Delete](./delete/)() | Raderar alla tecken i området. |
| [get_Bookmarks](./get_bookmarks/)() | Returnerar en [Bookmarks](./get_bookmarks/) samling som representerar alla bokmärken i området. |
| [get_Fields](./get_fields/)() | Returnerar en [Fields](./get_fields/) samling som representerar alla fält i området. |
| [get_FormFields](./get_formfields/)() | Returnerar en [FormFields](./get_formfields/) samling som representerar alla formulärfält i området. |
| [get_Revisions](./get_revisions/)() | Hämtar en samling av revisioner (spårade ändringar) som finns i detta område. |
| [get_StructuredDocumentTags](./get_structureddocumenttags/)() | Returnerar en [StructuredDocumentTags](./get_structureddocumenttags/) samling som representerar alla strukturerade dokumenttaggar i området. |
| [get_Text](./get_text/)() | Hämtar texten i området. |
| [GetEnumerator](./getenumerator/)() override |  |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [NormalizeFieldTypes](./normalizefieldtypes/)() | Ändrar fälttypvärden [FieldType](../../aspose.words.fields/fieldchar/get_fieldtype/) för [FieldStart](../../aspose.words.fields/fieldstart/), [FieldSeparator](../../aspose.words.fields/fieldseparator/), [FieldEnd](../../aspose.words.fields/fieldend/) i detta område så att de motsvarar de fälttyper som finns i fältkoderna. |
| [Replace](./replace/)(const System::String\&, const System::String\&) | Ersätter alla förekomster av ett specificerat teckensträngsmönster med en ersättningssträng. |
| [Replace](./replace/)(const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) | Ersätter alla förekomster av ett teckenmönster specificerat med ett reguljärt uttryck med en annan sträng. |
| [Replace](./replace/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) | Ersätter alla förekomster av ett specificerat teckensträngsmönster med en ersättningssträng. |
| [Replace](./replace/)(const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) | Ersätter alla förekomster av ett teckenmönster specificerat med ett reguljärt uttryck med en annan sträng. |
| [ToDocument](./todocument/)() | Skapar ett nytt fullständigt dokument som innehåller området. |
| static [Type](./type/)() |  |
| [UnlinkFields](./unlinkfields/)() | Kopplar bort fält i detta område. |
| [UpdateFields](./updatefields/)() | Uppdaterar värdena för dokumentfält i detta område. |
## Anmärkningar


Dokumentet representeras av ett träd av noder och noderna erbjuder operationer för att arbeta med trädet, men vissa operationer är enklare att utföra om dokumentet behandlas som en sammanhängande sekvens av text.

[Range](./) is a "facade" interface that provide methods that treat the document or portions of the document as "flat" text regardless of the fact that the document nodes are stored in a tree-like object model.

[Range](./) does not contain any text or nodes, it is merely a view or "window" over a fragment of a document.

## Exempel



Visar hur man hämtar textinnehållet för alla noder som ett område täcker.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Hello world!");

ASSERT_EQ(u"Hello world!", doc->get_Range()->get_Text().Trim());
```

## Se även

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
