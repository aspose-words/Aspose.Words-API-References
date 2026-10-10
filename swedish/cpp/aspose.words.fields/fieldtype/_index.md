---
title: "Aspose::Words::Fields::FieldType enum"
linktitle: "FieldType"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::FieldType enum. Anger Microsoft Word-fälttyper i C++."
type: docs
weight: 130000
url: /sv/cpp/aspose.words.fields/fieldtype/
---
## FieldType enum


Anger Microsoft Word-fälttyper.

```cpp
enum class FieldType
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| FieldNone | 0 | [Field](../field/) typ är inte specificerad eller okänd. |
| FieldCannotParse | 1 | Anger att fältet inte kunde analyseras. |
| FieldAddin | 81 | Anger ADDIN-fältet. |
| FieldAddressBlock | 93 | Anger ADDRESSBLOCK-fältet. |
| FieldAdvance | 84 | Anger ADVANCE-fältet. |
| FieldAsk | 38 | Anger ASK-fältet. |
| FieldAuthor | 17 | Anger AUTHOR-fältet. |
| FieldAutoNum | 54 | Anger AUTONUM-fältet. |
| FieldAutoNumLegal | 53 | Anger AUTONUMLGL-fältet. |
| FieldAutoNumOutline | 52 | Anger AUTONUMOUT-fältet. |
| FieldAutoText | 79 | Anger AUTOTEXT-fältet. |
| FieldAutoTextList | 89 | Anger AUTOTEXTLIST-fältet. |
| FieldBarcode | 63 | Anger BARCODE-fältet. |
| FieldBibliography | 100500 | Anger BIBLIOGRAPHY-fältet. |
| FieldBidiOutline | 92 | Anger BIDIOUTLINE-fältet. |
| FieldCitation | 1980 | Anger CITATION-fältet. |
| FieldComments | 19 | Anger COMMENTS-fältet. |
| FieldCompare | 80 | Anger COMPARE-fältet. |
| FieldCreateDate | 21 | Anger CREATEDATE-fältet. |
| FieldData | 40 | Anger DATA-fältet. |
| FieldDatabase | 78 | Anger DATABASE-fältet. |
| FieldDate | 31 | Anger DATE-fältet. |
| FieldDDE | 45 | Anger DDE-fältet. |
| FieldDisplayBarcode | 6301 | Anger DISPLAYBARCODE-fältet. |
| FieldMergeBarcode | 6302 | Anger MERGEBARCODE-fältet. |
| FieldDDEAuto | 46 | Anger DDEAUTO-fältet. |
| FieldDocProperty | 85 | Anger DOCPROPERTY-fältet. |
| FieldDocVariable | 64 | Anger DOCVARIABLE-fältet. |
| FieldEditTime | 25 | Anger EDITTIME-fältet. |
| FieldEmbed | 58 | Specificerar EMBED-fältet. |
| FieldEquation | 49 | Specificerar EQ-fältet. |
| FieldFileName | 29 | Specificerar FILENAME-fältet. |
| FieldFileSize | 69 | Specificerar FILESIZE-fältet. |
| FieldFillIn | 39 | Specificerar FILLIN-fältet. |
| FieldFootnoteRef | 5 | Specificerar FOOTNOTEREF-fältet. |
| FieldFormCheckBox | 71 | Specificerar FORMCHECKBOX-fältet. |
| FieldFormDropDown | 83 | Specificerar FORMDROPDOWN-fältet. |
| FieldFormTextInput | 70 | Specificerar FORMTEXT-fältet. |
| FieldFormula | 34 | Specificerar = (formel)-fältet. |
| FieldGreetingLine | 94 | Specificerar GREETINGLINE-fältet. |
| FieldGlossary | 47 | Specificerar GLOSSARY-fältet. |
| FieldGoToButton | 50 | Specificerar GOTOBUTTON-fältet. |
| FieldHtmlActiveX | 91 | Specificerar fältet som representerar en HTML-kontroll. |
| FieldHyperlink | 88 | Specificerar HYPERLINK-fältet. |
| FieldIf | 7 | Specificerar IF-fältet. |
| FieldInclude | 36 | Specificerar INCLUDE-fältet. |
| FieldIncludePicture | 67 | Specificerar INCLUDEPICTURE-fältet. |
| FieldIncludeText | 68 | Specificerar INCLUDETEXT-fältet. |
| FieldIndex | 8 | Anger INDEX-fältet. |
| FieldIndexEntry | 4 | Anger XE-fältet. |
| FieldInfo | 14 | Anger INFO-fältet. |
| FieldImport | 55 | Anger IMPORT-fältet. |
| FieldKeyword | 18 | Anger KEYWORDS-fältet. |
| FieldLastSavedBy | 20 | Anger LASTSAVEDBY-fältet. |
| FieldLink | 56 | Anger LINK-fältet. |
| FieldListNum | 90 | Anger LISTNUM-fältet. |
| FieldMacroButton | 51 | Anger MACROBUTTON-fältet. |
| FieldMergeField | 59 | Anger MERGEFIELD-fältet. |
| FieldMergeRec | 44 | Anger MERGEREC-fältet. |
| FieldMergeSeq | 75 | Anger MERGESEQ-fältet. |
| FieldNext | 41 | Anger NEXT-fältet. |
| FieldNextIf | 42 | Anger NEXTIF-fältet. |
| FieldNoteRef | 72 | Anger NOTEREF-fältet. |
| FieldNumChars | 28 | Anger NUMCHARS-fältet. |
| FieldNumPages | 26 | Anger NUMPAGES-fältet. |
| FieldNumWords | 27 | Specificerar fältet NUMWORDS. |
| FieldOcx | 87 | Specificerar fältet OCX. Normalt kommer Aspose.Words att representera en ActiveX‑kontroll som ett [Shape](../../aspose.words.drawing/shape/)‑objekt, men för vissa dokument där en kontroll saknar data och/eller verkar vara ogiltig, kommer den att representeras som ett fält. |
| FieldPage | 33 | Specificerar fältet PAGE. |
| FieldPageRef | 37 | Specificerar fältet PAGEREF. |
| FieldPrint | 48 | Specificerar fältet PRINT. |
| FieldPrintDate | 23 | Specificerar fältet PRINTDATE. |
| FieldPrivate | 77 | Specificerar fältet PRIVATE. |
| FieldQuote | 35 | Specificerar fältet QUOTE. |
| FieldRef | 3 | Specificerar fältet REF. |
| FieldRefNoKeyword | 2 | Specificerar att fältet representerar ett REF‑fält där nyckelordet har utelämnats. |
| FieldRefDoc | 11 | Specificerar fältet RD. |
| FieldRevisionNum | 24 | Specificerar fältet REVNUM. |
| FieldSaveDate | 22 | Specificerar fältet SAVEDATE. |
| FieldSection | 65 | Specificerar fältet SECTION. |
| FieldSectionPages | 66 | Specificerar fältet SECTIONPAGES. |
| FieldSequence | 12 | Specificerar fältet SEQ. |
| FieldSet | 6 | Anger SET-fältet. |
| FieldShape | 95 | Anger SHAPE-fältet. |
| FieldSkipIf | 43 | Anger SKIPIF-fältet. |
| FieldStyleRef | 10 | Anger STYLEREF-fältet. |
| FieldSubject | 16 | Anger SUBJECT-fältet. |
| FieldSymbol | 57 | Anger SYMBOL-fältet. |
| FieldTemplate | 30 | Anger TEMPLATE-fältet. |
| FieldTime | 32 | Anger TIME-fältet. |
| FieldTitle | 15 | Anger TITLE-fältet. |
| FieldTOA | 73 | Anger TOA-fältet. |
| FieldTOAEntry | 74 | Anger TA-fältet. |
| FieldTOC | 13 | Anger TOC-fältet. |
| FieldTOCEntry | 9 | Anger TC-fältet. |
| FieldUserAddress | 62 | Anger USERADDRESS-fältet. |
| FieldUserInitials | 61 | Anger USERINITIALS-fältet. |
| FieldUserName | 60 | Anger USERNAME-fältet. |


## Exempel



Visar hur man infogar ett fält i ett dokument med en fältkod.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Fields::Field> field = builder->InsertField(u"DATE \\@ \"dddd, MMMM dd, yyyy\"");

ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldDate, field->get_Type());
ASSERT_EQ(u"DATE \\@ \"dddd, MMMM dd, yyyy\"", field->GetFieldCode());

// Denna överlagring av InsertField‑metoden uppdaterar automatiskt infogade fält.
ASSERT_TRUE((System::DateTime::get_Today() - System::DateTime::Parse(field->get_Result())).get_Days() <= 1);
```


Visar hur man arbetar med en [FieldStart](../fieldstart/) nod.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto field = System::ExplicitCast<Aspose::Words::Fields::FieldDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDate, true));
field->get_Format()->set_DateTimeFormat(u"dddd, MMMM dd, yyyy");
field->Update();

System::SharedPtr<Aspose::Words::Fields::FieldChar> fieldStart = field->get_Start();

ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldDate, fieldStart->get_FieldType());
ASPOSE_ASSERT_EQ(false, fieldStart->get_IsDirty());
ASPOSE_ASSERT_EQ(false, fieldStart->get_IsLocked());

// Hämta fasadobjektet som representerar fältet i dokumentet.
field = System::ExplicitCast<Aspose::Words::Fields::FieldDate>(fieldStart->GetField());

ASPOSE_ASSERT_EQ(false, field->get_IsLocked());
ASSERT_EQ(u" DATE  \\@ \"dddd, MMMM dd, yyyy\"", field->GetFieldCode());

// Uppdatera fältet så att det visar det aktuella datumet.
field->Update();
```

## Se även

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
