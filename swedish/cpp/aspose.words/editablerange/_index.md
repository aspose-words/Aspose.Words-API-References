---
title: "Aspose::Words::EditableRange‑klass"
linktitle: "EditableRange"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::EditableRange‑klass. Representerar ett enda redigerbart område. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 24000
url: /sv/cpp/aspose.words/editablerange/
---
## EditableRange class


Representerar ett enda redigerbart område. För att läsa mer, besök artikeln [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/) i dokumentationen.

```cpp
class EditableRange : public System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [get_EditableRangeEnd](./get_editablerangeend/)() | Hämtar noden som representerar slutet av det redigerbara området. |
| [get_EditableRangeStart](./get_editablerangestart/)() const | Hämtar noden som representerar början av det redigerbara området. |
| [get_EditorGroup](./get_editorgroup/)() | Returnerar eller anger ett alias (eller redigeringsgrupp) som ska användas för att avgöra om den aktuella användaren får redigera detta redigerbara område. |
| [get_Id](./get_id/)() | Hämtar identifieraren för det redigerbara området. |
| [get_SingleUser](./get_singleuser/)() | Returnerar eller anger den enda användaren för det redigerbara området. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)() | Tar bort det redigerbara området från dokumentet. Tar inte bort innehållet inom det redigerbara området. |
| [set_EditorGroup](./set_editorgroup/)(Aspose::Words::EditorType) | Sättare för [Aspose::Words::EditableRange::get_EditorGroup](./get_editorgroup/). |
| [set_SingleUser](./set_singleuser/)(const System::String\&) | Sättare för [Aspose::Words::EditableRange::get_SingleUser](./get_singleuser/). |
| static [Type](./type/)() |  |
## Anmärkningar


[EditableRange](./) is a "facade" object that encapsulates two nodes [EditableRangeStart](./get_editablerangestart/) and [EditableRangeEnd](./get_editablerangeend/) in a document tree and allows to work with an editable range as a single object.

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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
