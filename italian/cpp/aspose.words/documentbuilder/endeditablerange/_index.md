---
title: "Aspose::Words::DocumentBuilder::EndEditableRange method"
linktitle: "EndEditableRange"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::DocumentBuilder::EndEditableRange. Contrassegna la posizione corrente nel documento come fine di un intervallo modificabile in C++."
type: docs
weight: 6000
url: /it/cpp/aspose.words/documentbuilder/endeditablerange/
---
## DocumentBuilder::EndEditableRange() method


Segna la posizione corrente nel documento come fine intervallo modificabile.

```cpp
System::SharedPtr<Aspose::Words::EditableRangeEnd> Aspose::Words::DocumentBuilder::EndEditableRange()
```


### ReturnValue

Il nodo di fine intervallo modificabile appena creato.
## Note


Un intervallo modificabile in un documento può sovrapporsi e coprire qualsiasi intervallo. Per creare un intervallo modificabile valido è necessario chiamare sia il metodo [StartEditableRange](../starteditablerange/) sia il metodo [EndEditableRange](./) o [EndEditableRange()](../).

Un intervallo modificabile malformato verrà ignorato quando il documento viene salvato.

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

* Class [EditableRangeEnd](../../editablerangeend/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::EndEditableRange(const System::SharedPtr\<Aspose::Words::EditableRangeStart\>\&) method


Segna la posizione corrente nel documento come fine intervallo modificabile.

```cpp
System::SharedPtr<Aspose::Words::EditableRangeEnd> Aspose::Words::DocumentBuilder::EndEditableRange(const System::SharedPtr<Aspose::Words::EditableRangeStart> &start)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inizio | const System::SharedPtr\<Aspose::Words::EditableRangeStart\>\& | Questo inizio di intervallo modificabile. |

### ReturnValue

Il nodo di fine intervallo modificabile appena creato.
## Note


Utilizza questo overload durante la creazione di intervalli modificabili annidati.

Un intervallo modificabile in un documento può sovrapporsi e coprire qualsiasi intervallo. Per creare un intervallo modificabile valido è necessario chiamare sia il metodo [StartEditableRange](../starteditablerange/) sia il metodo [EndEditableRange](./) o [EndEditableRange()](../).

Un intervallo modificabile malformato verrà ignorato quando il documento viene salvato.

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

* Class [EditableRangeEnd](../../editablerangeend/)
* Class [EditableRangeStart](../../editablerangestart/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
