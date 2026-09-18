---
title: "Aspose::Words::DocumentBuilder::MoveToMergeField Methode"
linktitle: "MoveToMergeField"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::DocumentBuilder::MoveToMergeField Methode. Bewegt den Cursor an eine Position direkt hinter das angegebene Zusammenführungsfeld und entfernt das Zusammenführungsfeld in C++."
type: docs
weight: 58000
url: /de/cpp/aspose.words/documentbuilder/movetomergefield/
---
## DocumentBuilder::MoveToMergeField(const System::String\&) method


Bewegt den Cursor zu einer Position direkt hinter dem angegebenen Zusammenführungsfeld und entfernt das Zusammenführungsfeld.

```cpp
bool Aspose::Words::DocumentBuilder::MoveToMergeField(const System::String &fieldName)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fieldName | const System::String\& | Der Groß-/Kleinschreibungs-unabhängige Name des Mail‑Zusammenführungsfeldes. |

### ReturnValue

**true** if the merge field was found and the cursor was moved; **false** otherwise.
## Hinweise


Beachte, dass diese Methode das Zusammenführungsfeld aus dem Dokument löscht, nachdem der Cursor bewegt wurde.

## Beispiele



Zeigt, wie man MERGEFIELDs mit Daten mithilfe eines Document Builders anstelle eines Seriendrucks füllt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Fügen Sie einige MERGEFIELDS ein, die während eines Seriendrucks Daten aus Spalten mit demselben Namen in einer Datenquelle übernehmen,
// und füllen Sie sie anschließend manuell.
builder->InsertField(u" MERGEFIELD Chairman ");
builder->InsertField(u" MERGEFIELD ChiefFinancialOfficer ");
builder->InsertField(u" MERGEFIELD ChiefTechnologyOfficer ");

builder->MoveToMergeField(u"Chairman");
builder->set_Bold(true);
builder->Writeln(u"John Doe");

builder->MoveToMergeField(u"ChiefFinancialOfficer");
builder->set_Italic(true);
builder->Writeln(u"Jane Doe");

builder->MoveToMergeField(u"ChiefTechnologyOfficer");
builder->set_Italic(true);
builder->Writeln(u"John Bloggs");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.FillMergeFields.docx");
```

## Siehe auch

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::MoveToMergeField(const System::String\&, bool, bool) method


Verschiebt das Zusammenführungsfeld zum angegebenen Zusammenführungsfeld.

```cpp
bool Aspose::Words::DocumentBuilder::MoveToMergeField(const System::String &fieldName, bool isAfter, bool isDeleteField)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fieldName | const System::String\& | Der Groß-/Kleinschreibungs-unabhängige Name des Mail‑Zusammenführungsfeldes. |
| isAfter | bool | Wenn **true**, wird der Cursor nach dem Feldende positioniert. Wenn **false**, wird der Cursor vor dem Feldanfang positioniert. |
| isDeleteField | bool | Wenn **true**, wird das Zusammenführungsfeld gelöscht. |

### ReturnValue

**true** if the merge field was found and the cursor was moved; **false** otherwise.

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

## Siehe auch

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
