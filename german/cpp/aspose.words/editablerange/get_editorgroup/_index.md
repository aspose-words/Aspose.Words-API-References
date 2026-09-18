---
title: "Aspose::Words::EditableRange::get_EditorGroup-Methode"
linktitle: "get_EditorGroup"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::EditableRange::get_EditorGroup-Methode. Gibt einen Alias (oder Bearbeitungsgruppe) zurück oder setzt ihn, der verwendet wird, um zu bestimmen, ob der aktuelle Benutzer diesen editierbaren Bereich in C++ bearbeiten darf."
type: docs
weight: 4000
url: /de/cpp/aspose.words/editablerange/get_editorgroup/
---
## EditableRange::get_EditorGroup method


Liefert oder setzt einen Alias (oder Bearbeitungsgruppe), der verwendet wird, um zu bestimmen, ob der aktuelle Benutzer diesen editierbaren Bereich bearbeiten darf.

```cpp
Aspose::Words::EditorType Aspose::Words::EditableRange::get_EditorGroup()
```

## Hinweise


Einzelner Benutzer und Editorgruppe können für den jeweiligen bearbeitbaren Bereich nicht gleichzeitig festgelegt werden; ist das eine gesetzt, wird das andere gelöscht.

## Beispiele



Zeigt, wie verschachtelte editierbare Bereiche erstellt werden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
doc->Protect(Aspose::Words::ProtectionType::ReadOnly, u"MyPassword");

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(System::String(u"Hello world! Since we have set the document's protection level to read-only, ") + u"we cannot edit this paragraph without the password.");

// Erstelle zwei verschachtelte editierbare Bereiche.
System::SharedPtr<Aspose::Words::EditableRangeStart> outerEditableRangeStart = builder->StartEditableRange();
builder->Writeln(u"This paragraph inside the outer editable range and can be edited.");

System::SharedPtr<Aspose::Words::EditableRangeStart> innerEditableRangeStart = builder->StartEditableRange();
builder->Writeln(u"This paragraph inside both the outer and inner editable ranges and can be edited.");

// Derzeit befindet sich der Einfügecursor des Dokumenten‑Builders in mehr als einem laufenden editierbaren Bereich.
// Wenn wir in dieser Situation einen editierbaren Bereich beenden wollen,
// müssen wir angeben, welchen der Bereiche wir beenden möchten, indem wir dessen EditableRangeStart‑Knoten übergeben.
builder->EndEditableRange(innerEditableRangeStart);

builder->Writeln(u"This paragraph inside the outer editable range and can be edited.");

builder->EndEditableRange(outerEditableRangeStart);

builder->Writeln(u"This paragraph is outside any editable ranges, and cannot be edited.");

// Wenn ein Textabschnitt zwei überlappende editierbare Bereiche mit angegebenen Gruppen hat,
// wird die kombinierte Gruppe von Benutzern, die von beiden Gruppen ausgeschlossen sind, daran gehindert, ihn zu bearbeiten.
outerEditableRangeStart->get_EditableRange()->set_EditorGroup(Aspose::Words::EditorType::Everyone);
innerEditableRangeStart->get_EditableRange()->set_EditorGroup(Aspose::Words::EditorType::Contributors);

doc->Save(get_ArtifactsDir() + u"EditableRange.Nested.docx");
```

## Siehe auch

* Enum [EditorType](../../editortype/)
* Class [EditableRange](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
