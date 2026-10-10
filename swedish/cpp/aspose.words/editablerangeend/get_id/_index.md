---
title: "Aspose::Words::EditableRangeEnd::get_Id metod"
linktitle: "get_Id"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::EditableRangeEnd::get_Id metod. Anger identifieraren för det redigerbara området i C++."
type: docs
weight: 4000
url: /sv/cpp/aspose.words/editablerangeend/get_id/
---
## EditableRangeEnd::get_Id method


Anger identifieraren för det redigerbara området.

```cpp
int32_t Aspose::Words::EditableRangeEnd::get_Id() const
```


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

* Class [EditableRangeEnd](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
