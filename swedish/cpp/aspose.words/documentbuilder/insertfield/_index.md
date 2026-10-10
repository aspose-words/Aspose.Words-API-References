---
title: "Aspose::Words::DocumentBuilder::InsertField metod"
linktitle: "InsertField"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::DocumentBuilder::InsertField metod. Infogar ett Word-fält i ett dokument och uppdaterar valfritt fältresultatet i C++."
type: docs
weight: 34000
url: /sv/cpp/aspose.words/documentbuilder/insertfield/
---
## DocumentBuilder::InsertField(Aspose::Words::Fields::FieldType, bool) method


Infogar ett Word‑fält i ett dokument och uppdaterar eventuellt fältresultatet.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::DocumentBuilder::InsertField(Aspose::Words::Fields::FieldType fieldType, bool updateField)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| fieldType | Aspose::Words::Fields::FieldType | Typen av fältet som ska läggas till. |
| updateField | bool | Anger om fältet ska uppdateras omedelbart. |

### ReturnValue

Ett [Field](../../../aspose.words.fields/field/)‑objekt som representerar det infogade fältet.
## Anmärkningar


Denna metod infogar ett fält i ett dokument. Aspose.Words kan uppdatera fält av de flesta typer, men inte alla. För mer information, se [InsertField()](../)‑overloaden.

## Exempel



Visar hur man infogar ett fält i ett dokument med hjälp av FieldType.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Infoga två fält samtidigt som du skickar en flagga som bestämmer om de ska uppdateras när byggaren infogar dem.
// I vissa fall kan uppdatering av fält vara beräkningsintensiv, och det kan vara en bra idé att skjuta upp uppdateringen.
doc->get_BuiltInDocumentProperties()->set_Author(u"John Doe");
builder->Write(u"This document was written by ");
builder->InsertField(Aspose::Words::Fields::FieldType::FieldAuthor, updateInsertedFieldsImmediately);

builder->InsertParagraph();
builder->Write(u"\nThis is page ");
builder->InsertField(Aspose::Words::Fields::FieldType::FieldPage, updateInsertedFieldsImmediately);

ASSERT_EQ(u" AUTHOR ", doc->get_Range()->get_Fields()->idx_get(0)->GetFieldCode());
ASSERT_EQ(u" PAGE ", doc->get_Range()->get_Fields()->idx_get(1)->GetFieldCode());

if (updateInsertedFieldsImmediately)
{
    ASSERT_EQ(u"John Doe", doc->get_Range()->get_Fields()->idx_get(0)->get_Result());
    ASSERT_EQ(u"1", doc->get_Range()->get_Fields()->idx_get(1)->get_Result());
}
else
{
    ASSERT_EQ(System::String::Empty, doc->get_Range()->get_Fields()->idx_get(0)->get_Result());
    ASSERT_EQ(System::String::Empty, doc->get_Range()->get_Fields()->idx_get(1)->get_Result());

    // Vi kommer behöva uppdatera dessa fält manuellt med hjälp av uppdateringsmetoderna.
    doc->get_Range()->get_Fields()->idx_get(0)->Update();

    ASSERT_EQ(u"John Doe", doc->get_Range()->get_Fields()->idx_get(0)->get_Result());

    doc->UpdateFields();

    ASSERT_EQ(u"1", doc->get_Range()->get_Fields()->idx_get(1)->get_Result());
}
```

## Se även

* Class [Field](../../../aspose.words.fields/field/)
* Enum [FieldType](../../../aspose.words.fields/fieldtype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertField(const System::String\&) method


Infogar ett Word‑fält i ett dokument och uppdaterar fältresultatet.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::DocumentBuilder::InsertField(const System::String &fieldCode)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| fieldCode | const System::String\& | Fältkoden att infoga (utan måsvingar). |

### ReturnValue

Ett [Field](../../../aspose.words.fields/field/)‑objekt som representerar det infogade fältet.
## Anmärkningar


Denna metod infogar ett fält i ett dokument och uppdaterar fältresultatet omedelbart. Aspose.Words kan uppdatera fält av de flesta typer, men inte alla. För mer information, se [InsertField()](../)‑overloaden.

## Exempel



Visar hur man infogar fält och flyttar dokumentbyggarens markör till dem.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->InsertField(u"MERGEFIELD MyMergeField1 \\* MERGEFORMAT");
builder->InsertField(u"MERGEFIELD MyMergeField2 \\* MERGEFORMAT");

// Flytta markören till den första MERGEFIELD.
builder->MoveToMergeField(u"MyMergeField1", true, false);

// Observera att markören placeras omedelbart efter den första MERGEFIELD och före den andra.
ASPOSE_ASSERT_EQ(doc->get_Range()->get_Fields()->idx_get(1)->get_Start(), builder->get_CurrentNode());
ASPOSE_ASSERT_EQ(doc->get_Range()->get_Fields()->idx_get(0)->get_End(), builder->get_CurrentNode()->get_PreviousSibling());

// Om vi vill redigera fältets fältkod eller innehåll med byggaren,
// måste dess markör vara inne i ett fält.
// För att placera den i ett fält måste vi anropa dokumentbyggarens MoveTo‑metod
// och skicka fältets start‑ eller separatornod som argument.
builder->Write(u" Text between our merge fields. ");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.MergeFields.docx");
```


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

## Se även

* Class [Field](../../../aspose.words.fields/field/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertField(const System::String\&, const System::String\&) method


Infogar ett Word‑fält i ett dokument utan att uppdatera fältresultatet.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::DocumentBuilder::InsertField(const System::String &fieldCode, const System::String &fieldValue)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| fieldCode | const System::String\& | Fältkoden att infoga (utan måsvingar). |
| fieldValue | const System::String\& | Fältvärdet att infoga. Skicka **null** för fält som inte har något värde. |

### ReturnValue

Ett [Field](../../../aspose.words.fields/field/)‑objekt som representerar det infogade fältet.
## Anmärkningar


[Fields](../../../aspose.words.fields/) in Microsoft Word documents consist of a field code and a field result. The field code is like a formula and the field result is like the value that the formula produces. The field code may also contain field switches that are like additional instructions to perform a specific action.

Du kan växla mellan att visa fältkoder och resultat i ditt dokument i Microsoft Word med tangentbordsgenvägen Alt+F9. Fältkoder visas mellan måsvingar ( { } ).

För att skapa ett fält måste du ange en fälttyp, fältkod och ett \"platshållar\"‑fältvärde. Om du är osäker på syntaxen för en viss fältkod, skapa fältet i Microsoft Word först och växla för att se dess fältkod.

Aspose.Words kan beräkna fältresultat för de flesta fälttyper, men den här metoden uppdaterar inte fältresultatet automatiskt. Eftersom fältresultatet inte beräknas automatiskt förväntas du skicka ett strängvärde (eller till och med en tom sträng) som kommer att infogas i fältresultatet. Detta värde kommer att kvarstå i fältresultatet som en platshållare tills fältet uppdateras. För att uppdatera fältresultatet kan du anropa [Update](../../../aspose.words.fields/field/update/) på fältobjektet som returneras till dig eller [UpdateFields](../../document/updatefields/) för att uppdatera fält i hela dokumentet.

## Exempel



Visar hur man ställer in sidnumrering i en sektion.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Section 1, page 1.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Section 1, page 2.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Section 1, page 3.");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Writeln(u"Section 2, page 1.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Section 2, page 2.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Section 2, page 3.");

// Flytta dokumentbyggaren till den första sektionens primära sidhuvud,
// vilket varje sida i den sektionen kommer att visa.
builder->MoveToSection(0);
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);

// Infoga ett PAGE‑fält, som kommer att visa numret på den aktuella sidan.
builder->Write(u"Page ");
builder->InsertField(u"PAGE", u"");

// Konfigurera sektionen så att sidantalet som PAGE‑fält visar startar från 5.
// Konfigurera också alla PAGE‑fält att visa sina sidnummer med versala romerska siffror.
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();
pageSetup->set_RestartPageNumbering(true);
pageSetup->set_PageStartingNumber(5);
pageSetup->set_PageNumberStyle(Aspose::Words::NumberStyle::UppercaseRoman);

// Skapa ett annat primärt sidhuvud för den andra sektionen, med ett annat PAGE‑fält.
builder->MoveToSection(1);
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
builder->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);
builder->Write(u" - ");
builder->InsertField(u"PAGE", u"");
builder->Write(u" - ");

// Konfigurera sektionen så att sidantalet som PAGE‑fält visar startar från 10.
// Konfigurera också alla PAGE‑fält att visa sina sidnummer med arabiska siffror.
pageSetup = doc->get_Sections()->idx_get(1)->get_PageSetup();
pageSetup->set_PageStartingNumber(10);
pageSetup->set_RestartPageNumbering(true);
pageSetup->set_PageNumberStyle(Aspose::Words::NumberStyle::Arabic);

doc->Save(get_ArtifactsDir() + u"PageSetup.PageNumbering.docx");
```

## Se även

* Class [Field](../../../aspose.words.fields/field/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
