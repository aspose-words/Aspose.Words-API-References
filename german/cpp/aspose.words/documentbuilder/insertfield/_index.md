---
title: "Aspose::Words::DocumentBuilder::InsertField method"
linktitle: "InsertField"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::DocumentBuilder::InsertField-Methode. Fügt ein Word-Feld in ein Dokument ein und aktualisiert optional das Feldresultat in C++."
type: docs
weight: 34000
url: /de/cpp/aspose.words/documentbuilder/insertfield/
---
## DocumentBuilder::InsertField(Aspose::Words::Fields::FieldType, bool) method


Fügt ein Word‑Feld in ein Dokument ein und aktualisiert optional das Feldresultat.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::DocumentBuilder::InsertField(Aspose::Words::Fields::FieldType fieldType, bool updateField)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fieldType | Aspose::Words::Fields::FieldType | Der Typ des anzuhängenden Feldes. |
| updateField | bool | Gibt an, ob das Feld sofort aktualisiert werden soll. |

### ReturnValue

Ein [Field](../../../aspose.words.fields/field/)-Objekt, das das eingefügte Feld darstellt.
## Hinweise


Diese Methode fügt ein Feld in ein Dokument ein. Aspose.Words kann Felder der meisten Typen aktualisieren, jedoch nicht alle. Weitere Details finden Sie in der Überladung [InsertField()](../).

## Beispiele



Zeigt, wie man ein Feld in ein Dokument einfügt, indem man FieldType verwendet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Fügen Sie zwei Felder ein und übergeben Sie dabei ein Flag, das bestimmt, ob sie beim Einfügen durch den Builder aktualisiert werden.
// In einigen Fällen kann das Aktualisieren von Feldern rechenintensiv sein, und es kann sinnvoll sein, die Aktualisierung aufzuschieben.
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

    // Wir müssen diese Felder manuell mit den Aktualisierungsmethoden aktualisieren.
    doc->get_Range()->get_Fields()->idx_get(0)->Update();

    ASSERT_EQ(u"John Doe", doc->get_Range()->get_Fields()->idx_get(0)->get_Result());

    doc->UpdateFields();

    ASSERT_EQ(u"1", doc->get_Range()->get_Fields()->idx_get(1)->get_Result());
}
```

## Siehe auch

* Class [Field](../../../aspose.words.fields/field/)
* Enum [FieldType](../../../aspose.words.fields/fieldtype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertField(const System::String\&) method


Fügt ein Word‑Feld in ein Dokument ein und aktualisiert das Feldresultat.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::DocumentBuilder::InsertField(const System::String &fieldCode)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fieldCode | const System::String\& | Der einzufügende Feldcode (ohne geschweifte Klammern). |

### ReturnValue

Ein [Field](../../../aspose.words.fields/field/)-Objekt, das das eingefügte Feld darstellt.
## Hinweise


Diese Methode fügt ein Feld in ein Dokument ein und aktualisiert das Feldresultat sofort. Aspose.Words kann Felder der meisten Typen aktualisieren, jedoch nicht alle. Weitere Details finden Sie in der Überladung [InsertField()](../).

## Beispiele



Zeigt, wie man Felder einfügt und den Cursor des Document Builders zu ihnen bewegt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->InsertField(u"MERGEFIELD MyMergeField1 \\* MERGEFORMAT");
builder->InsertField(u"MERGEFIELD MyMergeField2 \\* MERGEFORMAT");

// Bewegen Sie den Cursor zum ersten MERGEFIELD.
builder->MoveToMergeField(u"MyMergeField1", true, false);

// Beachten Sie, dass der Cursor unmittelbar nach dem ersten MERGEFIELD und vor dem zweiten platziert wird.
ASPOSE_ASSERT_EQ(doc->get_Range()->get_Fields()->idx_get(1)->get_Start(), builder->get_CurrentNode());
ASPOSE_ASSERT_EQ(doc->get_Range()->get_Fields()->idx_get(0)->get_End(), builder->get_CurrentNode()->get_PreviousSibling());

// Wenn wir den Feldcode oder den Inhalt des Feldes mit dem Builder bearbeiten möchten,
// müsste sich sein Cursor innerhalb eines Feldes befinden.
// Um es in ein Feld zu platzieren, müssten wir die MoveTo-Methode des document builders aufrufen.
// und übergeben den Start- oder Trennknoten des Feldes als Argument.
builder->Write(u" Text between our merge fields. ");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.MergeFields.docx");
```


Zeigt, wie man ein Feld mithilfe eines Feldcodes in ein Dokument einfügt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Fields::Field> field = builder->InsertField(u"DATE \\@ \"dddd, MMMM dd, yyyy\"");

ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldDate, field->get_Type());
ASSERT_EQ(u"DATE \\@ \"dddd, MMMM dd, yyyy\"", field->GetFieldCode());

// Diese Überladung der InsertField-Methode aktualisiert eingefügte Felder automatisch.
ASSERT_TRUE((System::DateTime::get_Today() - System::DateTime::Parse(field->get_Result())).get_Days() <= 1);
```

## Siehe auch

* Class [Field](../../../aspose.words.fields/field/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertField(const System::String\&, const System::String\&) method


Fügt ein Word‑Feld in ein Dokument ein, ohne das Feldresultat zu aktualisieren.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::DocumentBuilder::InsertField(const System::String &fieldCode, const System::String &fieldValue)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fieldCode | const System::String\& | Der einzufügende Feldcode (ohne geschweifte Klammern). |
| fieldValue | const System::String\& | Der Feldwert, der eingefügt werden soll. Übergeben Sie **null** für Felder, die keinen Wert haben. |

### ReturnValue

Ein [Field](../../../aspose.words.fields/field/)-Objekt, das das eingefügte Feld darstellt.
## Hinweise


[Fields](../../../aspose.words.fields/) in Microsoft Word documents consist of a field code and a field result. The field code is like a formula and the field result is like the value that the formula produces. The field code may also contain field switches that are like additional instructions to perform a specific action.

Sie können in Ihrem Dokument in Microsoft Word zwischen der Anzeige von Feldcodes und Ergebnissen mit der Tastenkombination Alt+F9 umschalten. Feldcodes erscheinen zwischen geschweiften Klammern ( { } ).

Um ein Feld zu erstellen, müssen Sie einen Feldtyp, einen Feldcode und einen „Platzhalter“-Feldwert angeben. Wenn Sie sich über die Syntax eines bestimmten Feldcodes nicht sicher sind, erstellen Sie das Feld zunächst in Microsoft Word und wechseln Sie dann, um dessen Feldcode zu sehen.

Aspose.Words kann Feldresultate für die meisten Feldtypen berechnen, aber diese Methode aktualisiert das Feldresultat nicht automatisch. Da das Feldresultat nicht automatisch berechnet wird, sollten Sie einen Zeichenkettenwert (oder sogar eine leere Zeichenkette) übergeben, der in das Feldresultat eingefügt wird. Dieser Wert bleibt im Feldresultat als Platzhalter, bis das Feld aktualisiert wird. Um das Feldresultat zu aktualisieren, können Sie [Update](../../../aspose.words.fields/field/update/) auf dem zurückgegebenen Feldobjekt aufrufen oder [UpdateFields](../../document/updatefields/) verwenden, um Felder im gesamten Dokument zu aktualisieren.

## Beispiele



Zeigt, wie man die Seitennummerierung in einem Abschnitt einrichtet.
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

// Verschieben Sie den Document Builder zum primären Header des ersten Abschnitts,
// der von jeder Seite dieses Abschnitts angezeigt wird.
builder->MoveToSection(0);
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);

// Fügen Sie ein PAGE-Feld ein, das die Nummer der aktuellen Seite anzeigt.
builder->Write(u"Page ");
builder->InsertField(u"PAGE", u"");

// Konfigurieren Sie den Abschnitt so, dass die von PAGE-Feldern angezeigte Seitenzahl bei 5 beginnt.
// Konfigurieren Sie außerdem alle PAGE-Felder so, dass sie ihre Seitenzahlen mit Großbuchstaben‑römischen Ziffern anzeigen.
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();
pageSetup->set_RestartPageNumbering(true);
pageSetup->set_PageStartingNumber(5);
pageSetup->set_PageNumberStyle(Aspose::Words::NumberStyle::UppercaseRoman);

// Erstellen Sie eine weitere primäre Kopfzeile für den zweiten Abschnitt, mit einem weiteren PAGE-Feld.
builder->MoveToSection(1);
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
builder->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);
builder->Write(u" - ");
builder->InsertField(u"PAGE", u"");
builder->Write(u" - ");

// Konfigurieren Sie den Abschnitt so, dass die Seitenzahl, die PAGE-Felder anzeigen, bei 10 beginnt.
// Konfigurieren Sie außerdem alle PAGE-Felder so, dass sie ihre Seitenzahlen mit arabischen Ziffern anzeigen.
pageSetup = doc->get_Sections()->idx_get(1)->get_PageSetup();
pageSetup->set_PageStartingNumber(10);
pageSetup->set_RestartPageNumbering(true);
pageSetup->set_PageNumberStyle(Aspose::Words::NumberStyle::Arabic);

doc->Save(get_ArtifactsDir() + u"PageSetup.PageNumbering.docx");
```

## Siehe auch

* Class [Field](../../../aspose.words.fields/field/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
