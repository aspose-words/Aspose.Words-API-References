---
title: "Aspose::Words::DocumentBuilder::MoveToMergeField metod"
linktitle: "MoveToMergeField"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::DocumentBuilder::MoveToMergeField metod. Flyttar markören till en position precis efter det angivna sammanslagningsfältet och tar bort sammanslagningsfältet i C++."
type: docs
weight: 58000
url: /sv/cpp/aspose.words/documentbuilder/movetomergefield/
---
## DocumentBuilder::MoveToMergeField(const System::String\&) method


Flyttar markören till en position strax bortom det angivna sammanslagningsfältet och tar bort sammanslagningsfältet.

```cpp
bool Aspose::Words::DocumentBuilder::MoveToMergeField(const System::String &fieldName)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| fieldName | const System::String\& | Det skiftlägesokänsliga namnet på mail merge-fältet. |

### ReturnValue

**true** if the merge field was found and the cursor was moved; **false** otherwise.
## Anmärkningar


Observera att den här metoden tar bort sammanslagningsfältet från dokumentet efter att markören har flyttats.

## Exempel



Visar hur man fyller MERGEFIELDs med data med en dokumentbyggare istället för en mail merge.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Infoga några MERGEFIELDS, som accepterar data från kolumner med samma namn i en datakälla under en mail merge,
// och fyll sedan i dem manuellt.
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

## Se även

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::MoveToMergeField(const System::String\&, bool, bool) method


Flyttar sammanslagningsfältet till det angivna sammanslagningsfältet.

```cpp
bool Aspose::Words::DocumentBuilder::MoveToMergeField(const System::String &fieldName, bool isAfter, bool isDeleteField)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| fieldName | const System::String\& | Det skiftlägesokänsliga namnet på mail merge-fältet. |
| isAfter | bool | När **true**, flyttar markören till efter fältets slut. När **false**, flyttar markören till före fältets början. |
| isDeleteField | bool | När **true**, raderar sammanslagningsfältet. |

### ReturnValue

**true** if the merge field was found and the cursor was moved; **false** otherwise.

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

## Se även

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
