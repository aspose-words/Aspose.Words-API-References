---
title: "Metodo Aspose::Words::EditableRangeEnd::get_Id"
linktitle: "get_Id"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::EditableRangeEnd::get_Id. Specifica l'identificatore dell'intervallo modificabile in C++."
type: docs
weight: 4000
url: /it/cpp/aspose.words/editablerangeend/get_id/
---
## EditableRangeEnd::get_Id method


Specifica l'identificatore dell'intervallo modificabile.

```cpp
int32_t Aspose::Words::EditableRangeEnd::get_Id() const
```


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

* Class [EditableRangeEnd](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
