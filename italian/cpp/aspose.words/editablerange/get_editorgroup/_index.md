---
title: "Metodo Aspose::Words::EditableRange::get_EditorGroup"
linktitle: "get_EditorGroup"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::EditableRange::get_EditorGroup. Restituisce o imposta un alias (o gruppo di modifica) che verrà utilizzato per determinare se l'utente corrente è autorizzato a modificare questo intervallo modificabile in C++."
type: docs
weight: 4000
url: /it/cpp/aspose.words/editablerange/get_editorgroup/
---
## EditableRange::get_EditorGroup method


Restituisce o imposta un alias (o gruppo di modifica) che verrà usato per determinare se l'utente corrente può modificare questo intervallo modificabile.

```cpp
Aspose::Words::EditorType Aspose::Words::EditableRange::get_EditorGroup()
```

## Note


L'utente singolo e il gruppo di editor non possono essere impostati simultaneamente per l'intervallo modificabile specifico; se uno è impostato, l'altro verrà cancellato.

## Esempi



Mostra come creare intervalli modificabili nidificati.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
doc->Protect(Aspose::Words::ProtectionType::ReadOnly, u"MyPassword");

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(System::String(u"Hello world! Since we have set the document's protection level to read-only, ") + u"we cannot edit this paragraph without the password.");

// Crea due intervalli modificabili nidificati.
System::SharedPtr<Aspose::Words::EditableRangeStart> outerEditableRangeStart = builder->StartEditableRange();
builder->Writeln(u"This paragraph inside the outer editable range and can be edited.");

System::SharedPtr<Aspose::Words::EditableRangeStart> innerEditableRangeStart = builder->StartEditableRange();
builder->Writeln(u"This paragraph inside both the outer and inner editable ranges and can be edited.");

// Attualmente, il cursore di inserimento dei nodi del document builder si trova in più di un intervallo modificabile in corso.
// Quando vogliamo terminare un intervallo modificabile in questa situazione,
// dobbiamo specificare quale dei intervalli desideriamo terminare passando il suo nodo EditableRangeStart.
builder->EndEditableRange(innerEditableRangeStart);

builder->Writeln(u"This paragraph inside the outer editable range and can be edited.");

builder->EndEditableRange(outerEditableRangeStart);

builder->Writeln(u"This paragraph is outside any editable ranges, and cannot be edited.");

// Se una sezione di testo ha due intervalli modificabili sovrapposti con gruppi specificati,
// il gruppo combinato di utenti esclusi da entrambi i gruppi è impedito di modificarlo.
outerEditableRangeStart->get_EditableRange()->set_EditorGroup(Aspose::Words::EditorType::Everyone);
innerEditableRangeStart->get_EditableRange()->set_EditorGroup(Aspose::Words::EditorType::Contributors);

doc->Save(get_ArtifactsDir() + u"EditableRange.Nested.docx");
```

## Vedi anche

* Enum [EditorType](../../editortype/)
* Class [EditableRange](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
