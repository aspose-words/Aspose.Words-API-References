---
title: "Aspose::Words::DocumentBuilder::EndEditableRange metod"
linktitle: "EndEditableRange"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::DocumentBuilder::EndEditableRange metod. Markerar den aktuella positionen i dokumentet som ett redigerbart områdes slut i C++."
type: docs
weight: 6000
url: /sv/cpp/aspose.words/documentbuilder/endeditablerange/
---
## DocumentBuilder::EndEditableRange() method


Markerar den aktuella positionen i dokumentet som ett redigerbart områdesslut.

```cpp
System::SharedPtr<Aspose::Words::EditableRangeEnd> Aspose::Words::DocumentBuilder::EndEditableRange()
```


### ReturnValue

Den redigerbara områdesslutnod som just skapades.
## Anmärkningar


Redigerbart område i ett dokument kan överlappa och omfatta vilket område som helst. För att skapa ett giltigt redigerbart område måste du anropa både [StartEditableRange](../starteditablerange/) och [EndEditableRange](./) eller [EndEditableRange()](../) metoder.

Felaktigt bildat redigerbart område kommer att ignoreras när dokumentet sparas.

## Exempel



Visar hur man arbetar med ett redigerbart område.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
doc->Protect(Aspose::Words::ProtectionType::ReadOnly, u"MyPassword");

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(System::String(u"Hello world! Since we have set the document's protection level to read-only,") + u" we cannot edit this paragraph without the password.");

// Redigerbara områden låter oss lämna delar av skyddade dokument öppna för redigering.
System::SharedPtr<Aspose::Words::EditableRangeStart> editableRangeStart = builder->StartEditableRange();
builder->Writeln(u"This paragraph is inside an editable range, and can be edited.");
System::SharedPtr<Aspose::Words::EditableRangeEnd> editableRangeEnd = builder->EndEditableRange();

// Ett välformat redigerbart område har en startnod och en slutnod.
// Dessa noder har matchande ID:n och omfattar redigerbara noder.
System::SharedPtr<Aspose::Words::EditableRange> editableRange = editableRangeStart->get_EditableRange();

ASSERT_EQ(editableRangeStart->get_Id(), editableRange->get_Id());
ASSERT_EQ(editableRangeEnd->get_Id(), editableRange->get_Id());

// Olika delar av det redigerbara området länkar till varandra.
ASSERT_EQ(editableRangeStart->get_Id(), editableRange->get_EditableRangeStart()->get_Id());
ASSERT_EQ(editableRangeStart->get_Id(), editableRangeEnd->get_EditableRangeStart()->get_Id());
ASSERT_EQ(editableRange->get_Id(), editableRangeStart->get_EditableRange()->get_Id());
ASSERT_EQ(editableRangeEnd->get_Id(), editableRange->get_EditableRangeEnd()->get_Id());

// Vi kan komma åt nodtyperna för varje del på detta sätt. Det redigerbara området i sig är inte en nod,
// utan en entitet som består av en start, ett slut och deras inneslutna innehåll.
ASSERT_EQ(Aspose::Words::NodeType::EditableRangeStart, editableRangeStart->get_NodeType());
ASSERT_EQ(Aspose::Words::NodeType::EditableRangeEnd, editableRangeEnd->get_NodeType());

builder->Writeln(u"This paragraph is outside the editable range, and cannot be edited.");

doc->Save(get_ArtifactsDir() + u"EditableRange.CreateAndRemove.docx");

// Ta bort ett redigerbart område. Alla noder som var inom området kommer att förbli intakta.
editableRange->Remove();
```

## Se även

* Class [EditableRangeEnd](../../editablerangeend/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::EndEditableRange(const System::SharedPtr\<Aspose::Words::EditableRangeStart\>\&) method


Markerar den aktuella positionen i dokumentet som ett redigerbart områdesslut.

```cpp
System::SharedPtr<Aspose::Words::EditableRangeEnd> Aspose::Words::DocumentBuilder::EndEditableRange(const System::SharedPtr<Aspose::Words::EditableRangeStart> &start)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| start | const System::SharedPtr\<Aspose::Words::EditableRangeStart\>\& | Detta redigerbara områdesstart. |

### ReturnValue

Den redigerbara områdesslutnod som just skapades.
## Anmärkningar


Använd denna överlagring när du skapar nästlade redigerbara områden.

Redigerbart område i ett dokument kan överlappa och omfatta vilket område som helst. För att skapa ett giltigt redigerbart område måste du anropa både [StartEditableRange](../starteditablerange/) och [EndEditableRange](./) eller [EndEditableRange()](../) metoder.

Felaktigt bildat redigerbart område kommer att ignoreras när dokumentet sparas.

## Exempel



Visar hur man skapar nästlade redigerbara områden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
doc->Protect(Aspose::Words::ProtectionType::ReadOnly, u"MyPassword");

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(System::String(u"Hello world! Since we have set the document's protection level to read-only, ") + u"we cannot edit this paragraph without the password.");

// Skapa två nästlade redigerbara områden.
System::SharedPtr<Aspose::Words::EditableRangeStart> outerEditableRangeStart = builder->StartEditableRange();
builder->Writeln(u"This paragraph inside the outer editable range and can be edited.");

System::SharedPtr<Aspose::Words::EditableRangeStart> innerEditableRangeStart = builder->StartEditableRange();
builder->Writeln(u"This paragraph inside both the outer and inner editable ranges and can be edited.");

// För närvarande befinner sig dokumentbyggarens nodinfogningsmarkör i mer än ett pågående redigerbart område.
// När vi vill avsluta ett redigerbart område i denna situation,
// måste vi ange vilket av områdena vi vill avsluta genom att skicka dess EditableRangeStart-nod.
builder->EndEditableRange(innerEditableRangeStart);

builder->Writeln(u"This paragraph inside the outer editable range and can be edited.");

builder->EndEditableRange(outerEditableRangeStart);

builder->Writeln(u"This paragraph is outside any editable ranges, and cannot be edited.");

// Om ett textområde har två överlappande redigerbara områden med angivna grupper,
// så förhindras den kombinerade gruppen av användare som uteslutits av båda grupperna från att redigera det.
outerEditableRangeStart->get_EditableRange()->set_EditorGroup(Aspose::Words::EditorType::Everyone);
innerEditableRangeStart->get_EditableRange()->set_EditorGroup(Aspose::Words::EditorType::Contributors);

doc->Save(get_ArtifactsDir() + u"EditableRange.Nested.docx");
```

## Se även

* Class [EditableRangeEnd](../../editablerangeend/)
* Class [EditableRangeStart](../../editablerangestart/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
