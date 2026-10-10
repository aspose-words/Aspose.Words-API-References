---
title: "Aspose::Words::EditableRange::get_EditorGroup-metoden"
linktitle: "get_EditorGroup"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::EditableRange::get_EditorGroup-metoden. Returnerar eller anger ett alias (eller redigeringsgrupp) som ska användas för att avgöra om den aktuella användaren får redigera detta redigerbara område i C++."
type: docs
weight: 4000
url: /sv/cpp/aspose.words/editablerange/get_editorgroup/
---
## EditableRange::get_EditorGroup method


Returnerar eller anger ett alias (eller redigeringsgrupp) som ska användas för att avgöra om den aktuella användaren får redigera detta redigerbara område.

```cpp
Aspose::Words::EditorType Aspose::Words::EditableRange::get_EditorGroup()
```

## Anmärkningar


Enskild användare och redigeringsgrupp kan inte anges samtidigt för det specifika redigeringsområdet; om den ena är angiven, rensas den andra.

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

* Enum [EditorType](../../editortype/)
* Class [EditableRange](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
