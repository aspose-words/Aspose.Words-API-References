---
title: "Classe Aspose::Words::EditableRange"
linktitle: "EditableRange"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::EditableRange class. Rappresenta un singolo intervallo modificabile. Per saperne di più, visita l'articolo della documentazione in C++."
type: docs
weight: 24000
url: /it/cpp/aspose.words/editablerange/
---
## EditableRange class


Rappresenta un singolo intervallo modificabile. Per saperne di più, visita l'articolo di documentazione [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/).

```cpp
class EditableRange : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get_EditableRangeEnd](./get_editablerangeend/)() | Ottiene il nodo che rappresenta la fine dell'intervallo modificabile. |
| [get_EditableRangeStart](./get_editablerangestart/)() const | Ottiene il nodo che rappresenta l'inizio dell'intervallo modificabile. |
| [get_EditorGroup](./get_editorgroup/)() | Restituisce o imposta un alias (o gruppo di modifica) che verrà usato per determinare se l'utente corrente può modificare questo intervallo modificabile. |
| [get_Id](./get_id/)() | Ottiene l'identificatore dell'intervallo modificabile. |
| [get_SingleUser](./get_singleuser/)() | Restituisce o imposta l'utente unico per l'intervallo modificabile. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)() | Rimuove l'intervallo modificabile dal documento. Non rimuove il contenuto all'interno dell'intervallo modificabile. |
| [set_EditorGroup](./set_editorgroup/)(Aspose::Words::EditorType) | Impostatore per [Aspose::Words::EditableRange::get_EditorGroup](./get_editorgroup/). |
| [set_SingleUser](./set_singleuser/)(const System::String\&) | Impostatore per [Aspose::Words::EditableRange::get_SingleUser](./get_singleuser/). |
| static [Type](./type/)() |  |
## Note


[EditableRange](./) is a "facade" object that encapsulates two nodes [EditableRangeStart](./get_editablerangestart/) and [EditableRangeEnd](./get_editablerangeend/) in a document tree and allows to work with an editable range as a single object.

## Esempi



Mostra come lavorare con un intervallo modificabile.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
doc->Protect(Aspose::Words::ProtectionType::ReadOnly, u"MyPassword");

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(System::String(u"Hello world! Since we have set the document's protection level to read-only,") + u" we cannot edit this paragraph without the password.");

// Gli intervalli modificabili ci consentono di lasciare parti di documenti protetti aperte per la modifica.
System::SharedPtr<Aspose::Words::EditableRangeStart> editableRangeStart = builder->StartEditableRange();
builder->Writeln(u"This paragraph is inside an editable range, and can be edited.");
System::SharedPtr<Aspose::Words::EditableRangeEnd> editableRangeEnd = builder->EndEditableRange();

// Un intervallo modificabile ben formato ha un nodo di inizio e un nodo di fine.
// Questi nodi hanno ID corrispondenti e includono nodi modificabili.
System::SharedPtr<Aspose::Words::EditableRange> editableRange = editableRangeStart->get_EditableRange();

ASSERT_EQ(editableRangeStart->get_Id(), editableRange->get_Id());
ASSERT_EQ(editableRangeEnd->get_Id(), editableRange->get_Id());

// Le diverse parti dell'intervallo modificabile sono collegate tra loro.
ASSERT_EQ(editableRangeStart->get_Id(), editableRange->get_EditableRangeStart()->get_Id());
ASSERT_EQ(editableRangeStart->get_Id(), editableRangeEnd->get_EditableRangeStart()->get_Id());
ASSERT_EQ(editableRange->get_Id(), editableRangeStart->get_EditableRange()->get_Id());
ASSERT_EQ(editableRangeEnd->get_Id(), editableRange->get_EditableRangeEnd()->get_Id());

// Possiamo accedere ai tipi di nodo di ogni parte in questo modo. L'intervallo modificabile stesso non è un nodo,
// ma un'entità che consiste in un inizio, una fine e i loro contenuti inclusi.
ASSERT_EQ(Aspose::Words::NodeType::EditableRangeStart, editableRangeStart->get_NodeType());
ASSERT_EQ(Aspose::Words::NodeType::EditableRangeEnd, editableRangeEnd->get_NodeType());

builder->Writeln(u"This paragraph is outside the editable range, and cannot be edited.");

doc->Save(get_ArtifactsDir() + u"EditableRange.CreateAndRemove.docx");

// Rimuovi un intervallo modificabile. Tutti i nodi che erano all'interno dell'intervallo rimarranno intatti.
editableRange->Remove();
```

## Vedi anche

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
