---
title: "Aspose::Words::Fields::FieldType enum"
linktitle: "FieldType"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Fields::FieldType enum. يحدد أنواع حقول Microsoft Word في C++."
type: docs
weight: 130000
url: /ar/cpp/aspose.words.fields/fieldtype/
---
## FieldType enum


يحدد أنواع حقول Microsoft Word.

```cpp
enum class FieldType
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| FieldNone | 0 | [Field](../field/) النوع غير محدد أو غير معروف. |
| FieldCannotParse | 1 | يحدد أن الحقل لم يتمكن من التحليل. |
| FieldAddin | 81 | يحدد حقل ADDIN. |
| FieldAddressBlock | 93 | يحدد حقل ADDRESSBLOCK. |
| FieldAdvance | 84 | يحدد حقل ADVANCE. |
| FieldAsk | 38 | يحدد حقل ASK. |
| FieldAuthor | 17 | يحدد حقل AUTHOR. |
| FieldAutoNum | 54 | يحدد حقل AUTONUM. |
| FieldAutoNumLegal | 53 | يحدد حقل AUTONUMLGL. |
| FieldAutoNumOutline | 52 | يحدد حقل AUTONUMOUT. |
| FieldAutoText | 79 | يحدد حقل AUTOTEXT. |
| FieldAutoTextList | 89 | يحدد حقل AUTOTEXTLIST. |
| FieldBarcode | 63 | يحدد حقل BARCODE. |
| FieldBibliography | 100500 | يحدد حقل BIBLIOGRAPHY. |
| FieldBidiOutline | 92 | يحدد حقل BIDIOUTLINE. |
| FieldCitation | 1980 | يحدد حقل CITATION. |
| FieldComments | 19 | يحدد حقل COMMENTS. |
| FieldCompare | 80 | يحدد حقل COMPARE. |
| FieldCreateDate | 21 | يحدد حقل CREATEDATE. |
| FieldData | 40 | يحدد حقل DATA. |
| FieldDatabase | 78 | يحدد حقل DATABASE. |
| FieldDate | 31 | يحدد حقل DATE. |
| FieldDDE | 45 | يحدد حقل DDE. |
| FieldDisplayBarcode | 6301 | يحدد حقل DISPLAYBARCODE. |
| FieldMergeBarcode | 6302 | يحدد حقل MERGEBARCODE. |
| FieldDDEAuto | 46 | يحدد حقل DDEAUTO. |
| FieldDocProperty | 85 | يحدد حقل DOCPROPERTY. |
| FieldDocVariable | 64 | يحدد حقل DOCVARIABLE. |
| FieldEditTime | 25 | يحدد حقل EDITTIME. |
| FieldEmbed | 58 | يحدد حقل EMBED. |
| FieldEquation | 49 | يحدد حقل EQ. |
| FieldFileName | 29 | يحدد حقل FILENAME. |
| FieldFileSize | 69 | يحدد حقل FILESIZE. |
| FieldFillIn | 39 | يحدد حقل FILLIN. |
| FieldFootnoteRef | 5 | يحدد حقل FOOTNOTEREF. |
| FieldFormCheckBox | 71 | يحدد حقل FORMCHECKBOX. |
| FieldFormDropDown | 83 | يحدد حقل FORMDROPDOWN. |
| FieldFormTextInput | 70 | يحدد حقل FORMTEXT. |
| FieldFormula | 34 | يحدد حقل = (الصيغة). |
| FieldGreetingLine | 94 | يحدد حقل GREETINGLINE. |
| FieldGlossary | 47 | يحدد حقل GLOSSARY. |
| FieldGoToButton | 50 | يحدد حقل GOTOBUTTON. |
| FieldHtmlActiveX | 91 | يحدد الحقل الذي يمثل عنصر تحكم HTML. |
| FieldHyperlink | 88 | يحدد حقل HYPERLINK. |
| FieldIf | 7 | يحدد حقل IF. |
| FieldInclude | 36 | يحدد حقل INCLUDE. |
| FieldIncludePicture | 67 | يحدد حقل INCLUDEPICTURE. |
| FieldIncludeText | 68 | يحدد حقل INCLUDETEXT. |
| FieldIndex | 8 | يحدد حقل INDEX. |
| FieldIndexEntry | 4 | يحدد حقل XE. |
| FieldInfo | 14 | يحدد حقل INFO. |
| FieldImport | 55 | يحدد حقل IMPORT. |
| FieldKeyword | 18 | يحدد حقل KEYWORDS. |
| FieldLastSavedBy | 20 | يحدد حقل LASTSAVEDBY. |
| FieldLink | 56 | يحدد حقل LINK. |
| FieldListNum | 90 | يحدد حقل LISTNUM. |
| FieldMacroButton | 51 | يحدد حقل MACROBUTTON. |
| FieldMergeField | 59 | يحدد حقل MERGEFIELD. |
| FieldMergeRec | 44 | يحدد حقل MERGEREC. |
| FieldMergeSeq | 75 | يحدد حقل MERGESEQ. |
| FieldNext | 41 | يحدد حقل NEXT. |
| FieldNextIf | 42 | يحدد حقل NEXTIF. |
| FieldNoteRef | 72 | يحدد حقل NOTEREF. |
| FieldNumChars | 28 | يحدد حقل NUMCHARS. |
| FieldNumPages | 26 | يحدد حقل NUMPAGES. |
| FieldNumWords | 27 | يحدد حقل NUMWORDS. |
| FieldOcx | 87 | يحدد حقل OCX. عادةً، Aspose.Words سيقوم بتمثيل عنصر تحكم ActiveX ككائن [Shape](../../aspose.words.drawing/shape/)، ولكن لبعض المستندات، حيث لا يحتوي التحكم على بيانات أو يبدو غير صالح، سيتم تمثيله كحقل. |
| FieldPage | 33 | يحدد حقل PAGE. |
| FieldPageRef | 37 | يحدد حقل PAGEREF. |
| FieldPrint | 48 | يحدد حقل PRINT. |
| FieldPrintDate | 23 | يحدد حقل PRINTDATE. |
| FieldPrivate | 77 | يحدد حقل PRIVATE. |
| FieldQuote | 35 | يحدد حقل QUOTE. |
| FieldRef | 3 | يحدد حقل REF. |
| FieldRefNoKeyword | 2 | يحدد أن الحقل يمثل حقل REF حيث تم حذف الكلمة المفتاحية. |
| FieldRefDoc | 11 | يحدد حقل RD. |
| FieldRevisionNum | 24 | يحدد حقل REVNUM. |
| FieldSaveDate | 22 | يحدد حقل SAVEDATE. |
| FieldSection | 65 | يحدد حقل SECTION. |
| FieldSectionPages | 66 | يحدد حقل SECTIONPAGES. |
| FieldSequence | 12 | يحدد حقل SEQ. |
| FieldSet | 6 | يحدد حقل SET. |
| FieldShape | 95 | يحدد حقل SHAPE. |
| FieldSkipIf | 43 | يحدد حقل SKIPIF. |
| FieldStyleRef | 10 | يحدد حقل STYLEREF. |
| FieldSubject | 16 | يحدد حقل SUBJECT. |
| FieldSymbol | 57 | يحدد حقل SYMBOL. |
| FieldTemplate | 30 | يحدد حقل TEMPLATE. |
| FieldTime | 32 | يحدد حقل TIME. |
| FieldTitle | 15 | يحدد حقل TITLE. |
| FieldTOA | 73 | يحدد حقل TOA. |
| FieldTOAEntry | 74 | يحدد حقل TA. |
| FieldTOC | 13 | يحدد حقل TOC. |
| FieldTOCEntry | 9 | يحدد حقل TC. |
| FieldUserAddress | 62 | يحدد حقل USERADDRESS. |
| FieldUserInitials | 61 | يحدد حقل USERINITIALS. |
| FieldUserName | 60 | يحدد حقل USERNAME. |


## أمثلة



يظهر كيفية إدراج حقل في مستند باستخدام رمز الحقل.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Fields::Field> field = builder->InsertField(u"DATE \\@ \"dddd, MMMM dd, yyyy\"");

ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldDate, field->get_Type());
ASSERT_EQ(u"DATE \\@ \"dddd, MMMM dd, yyyy\"", field->GetFieldCode());

// هذا التحميل الزائد لطريقة InsertField يقوم تلقائيًا بتحديث الحقول المدخلة.
ASSERT_TRUE((System::DateTime::get_Today() - System::DateTime::Parse(field->get_Result())).get_Days() <= 1);
```


يظهر كيفية العمل مع عقدة [FieldStart](../fieldstart/).
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

// استرجع كائن الواجهة الذي يمثل الحقل في المستند.
field = System::ExplicitCast<Aspose::Words::Fields::FieldDate>(fieldStart->GetField());

ASPOSE_ASSERT_EQ(false, field->get_IsLocked());
ASSERT_EQ(u" DATE  \\@ \"dddd, MMMM dd, yyyy\"", field->GetFieldCode());

// حدّث الحقل لعرض التاريخ الحالي.
field->Update();
```

## انظر أيضًا

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
