---
title: "Aspose::Words::EditableRange‑Klasse"
linktitle: "EditableRange"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::EditableRange‑Klasse. Stellt einen einzelnen editierbaren Bereich dar. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 24000
url: /de/cpp/aspose.words/editablerange/
---
## EditableRange class


Stellt einen einzelnen bearbeitbaren Bereich dar. Weitere Informationen finden Sie im Dokumentationsartikel [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/).

```cpp
class EditableRange : public System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get_EditableRangeEnd](./get_editablerangeend/)() | Gibt den Knoten zurück, der das Ende des editierbaren Bereichs darstellt. |
| [get_EditableRangeStart](./get_editablerangestart/)() const | Gibt den Knoten zurück, der den Anfang des editierbaren Bereichs darstellt. |
| [get_EditorGroup](./get_editorgroup/)() | Liefert oder setzt einen Alias (oder Bearbeitungsgruppe), der verwendet wird, um zu bestimmen, ob der aktuelle Benutzer diesen editierbaren Bereich bearbeiten darf. |
| [get_Id](./get_id/)() | Gibt die Kennung des editierbaren Bereichs zurück. |
| [get_SingleUser](./get_singleuser/)() | Liefert oder setzt den einzelnen Benutzer für den editierbaren Bereich. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)() | Entfernt den editierbaren Bereich aus dem Dokument. Der Inhalt innerhalb des editierbaren Bereichs wird nicht entfernt. |
| [set_EditorGroup](./set_editorgroup/)(Aspose::Words::EditorType) | Setter für [Aspose::Words::EditableRange::get_EditorGroup](./get_editorgroup/). |
| [set_SingleUser](./set_singleuser/)(const System::String\&) | Setter für [Aspose::Words::EditableRange::get_SingleUser](./get_singleuser/). |
| static [Type](./type/)() |  |
## Hinweise


[EditableRange](./) is a "facade" object that encapsulates two nodes [EditableRangeStart](./get_editablerangestart/) and [EditableRangeEnd](./get_editablerangeend/) in a document tree and allows to work with an editable range as a single object.

## Beispiele



Zeigt, wie man mit einem editierbaren Bereich arbeitet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
doc->Protect(Aspose::Words::ProtectionType::ReadOnly, u"MyPassword");

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(System::String(u"Hello world! Since we have set the document's protection level to read-only,") + u" we cannot edit this paragraph without the password.");

// Editierbare Bereiche ermöglichen es uns, Teile geschützter Dokumente zum Bearbeiten freizugeben.
System::SharedPtr<Aspose::Words::EditableRangeStart> editableRangeStart = builder->StartEditableRange();
builder->Writeln(u"This paragraph is inside an editable range, and can be edited.");
System::SharedPtr<Aspose::Words::EditableRangeEnd> editableRangeEnd = builder->EndEditableRange();

// Ein korrekt aufgebauter editierbarer Bereich hat einen Startknoten und einen Endknoten.
// Diese Knoten besitzen passende IDs und umfassen editierbare Knoten.
System::SharedPtr<Aspose::Words::EditableRange> editableRange = editableRangeStart->get_EditableRange();

ASSERT_EQ(editableRangeStart->get_Id(), editableRange->get_Id());
ASSERT_EQ(editableRangeEnd->get_Id(), editableRange->get_Id());

// Verschiedene Teile des editierbaren Bereichs verlinken miteinander.
ASSERT_EQ(editableRangeStart->get_Id(), editableRange->get_EditableRangeStart()->get_Id());
ASSERT_EQ(editableRangeStart->get_Id(), editableRangeEnd->get_EditableRangeStart()->get_Id());
ASSERT_EQ(editableRange->get_Id(), editableRangeStart->get_EditableRange()->get_Id());
ASSERT_EQ(editableRangeEnd->get_Id(), editableRange->get_EditableRangeEnd()->get_Id());

// Wir können die Knotentypen jedes Teils so abrufen. Der editierbare Bereich selbst ist kein Knoten,
// sondern eine Entität, die aus einem Start, einem Ende und deren eingeschlossenen Inhalten besteht.
ASSERT_EQ(Aspose::Words::NodeType::EditableRangeStart, editableRangeStart->get_NodeType());
ASSERT_EQ(Aspose::Words::NodeType::EditableRangeEnd, editableRangeEnd->get_NodeType());

builder->Writeln(u"This paragraph is outside the editable range, and cannot be edited.");

doc->Save(get_ArtifactsDir() + u"EditableRange.CreateAndRemove.docx");

// Entfernen Sie einen editierbaren Bereich. Alle Knoten, die sich innerhalb des Bereichs befanden, bleiben unverändert.
editableRange->Remove();
```

## Siehe auch

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
