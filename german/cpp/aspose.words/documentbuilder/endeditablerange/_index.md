---
title: "Aspose::Words::DocumentBuilder::EndEditableRange Methode"
linktitle: "EndEditableRange"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::DocumentBuilder::EndEditableRange Methode. Markiert die aktuelle Position im Dokument als Ende eines bearbeitbaren Bereichs in C++."
type: docs
weight: 6000
url: /de/cpp/aspose.words/documentbuilder/endeditablerange/
---
## DocumentBuilder::EndEditableRange() method


Markiert die aktuelle Position im Dokument als Ende eines bearbeitbaren Bereichs.

```cpp
System::SharedPtr<Aspose::Words::EditableRangeEnd> Aspose::Words::DocumentBuilder::EndEditableRange()
```


### ReturnValue

Der gerade erstellte Endknoten des bearbeitbaren Bereichs.
## Hinweise


Ein bearbeitbarer Bereich in einem Dokument kann überlappen und beliebige Bereiche umfassen. Um einen gültigen bearbeitbaren Bereich zu erstellen, müssen Sie sowohl die Methoden [StartEditableRange](../starteditablerange/) und [EndEditableRange](./) als auch [EndEditableRange()](../) aufrufen.

Ein fehlerhaft formulierter bearbeitbarer Bereich wird beim Speichern des Dokuments ignoriert.

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

* Class [EditableRangeEnd](../../editablerangeend/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::EndEditableRange(const System::SharedPtr\<Aspose::Words::EditableRangeStart\>\&) method


Markiert die aktuelle Position im Dokument als Ende eines bearbeitbaren Bereichs.

```cpp
System::SharedPtr<Aspose::Words::EditableRangeEnd> Aspose::Words::DocumentBuilder::EndEditableRange(const System::SharedPtr<Aspose::Words::EditableRangeStart> &start)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Start | const System::SharedPtr\<Aspose::Words::EditableRangeStart\>\& | Dieser Start des bearbeitbaren Bereichs. |

### ReturnValue

Der gerade erstellte Endknoten des bearbeitbaren Bereichs.
## Hinweise


Verwenden Sie diese Überladung beim Erstellen verschachtelter bearbeitbarer Bereiche.

Ein bearbeitbarer Bereich in einem Dokument kann überlappen und beliebige Bereiche umfassen. Um einen gültigen bearbeitbaren Bereich zu erstellen, müssen Sie sowohl die Methoden [StartEditableRange](../starteditablerange/) und [EndEditableRange](./) als auch [EndEditableRange()](../) aufrufen.

Ein fehlerhaft formulierter bearbeitbarer Bereich wird beim Speichern des Dokuments ignoriert.

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

* Class [EditableRangeEnd](../../editablerangeend/)
* Class [EditableRangeStart](../../editablerangestart/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
