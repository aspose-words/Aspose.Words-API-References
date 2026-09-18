---
title: "Aspose::Words::EditableRangeEnd::get_EditableRangeStart Methode"
linktitle: "get_EditableRangeStart"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::EditableRangeEnd::get_EditableRangeStart Methode. Entsprechendes EditableRangeStart, anhand der ID in C++ erhalten."
type: docs
weight: 3000
url: /de/cpp/aspose.words/editablerangeend/get_editablerangestart/
---
## EditableRangeEnd::get_EditableRangeStart method


Entsprechendes [EditableRangeStart](../../editablerangestart/), anhand der ID erhalten.

```cpp
System::SharedPtr<Aspose::Words::EditableRangeStart> Aspose::Words::EditableRangeEnd::get_EditableRangeStart()
```


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

* Class [EditableRangeStart](../../editablerangestart/)
* Class [EditableRangeEnd](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
