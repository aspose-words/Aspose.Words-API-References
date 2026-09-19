---
title: "Aspose::Words::DocumentVisitor::VisitFieldStart metodo"
linktitle: "VisitFieldStart"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::DocumentVisitor::VisitFieldStart metodo. Chiamato quando un campo inizia nel documento in C++."
type: docs
weight: 23000
url: /it/cpp/aspose.words/documentvisitor/visitfieldstart/
---
## DocumentVisitor::VisitFieldStart method


Chiamato quando inizia un campo nel documento.

```cpp
virtual Aspose::Words::VisitorAction Aspose::Words::DocumentVisitor::VisitFieldStart(System::SharedPtr<Aspose::Words::Fields::FieldStart> fieldStart)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fieldStart | System::SharedPtr\<Aspose::Words::Fields::FieldStart\> | L'oggetto che viene visitato. |

### ReturnValue

Un valore [VisitorAction](../../visitoraction/) che specifica come continuare l'enumerazione.
## Note


Un campo in un documento Word è composto da un codice di campo e da un valore di campo.

Ad esempio, un campo che visualizza il numero di pagina può essere rappresentato come segue:

[FieldStart]PAGE[FieldSeparator]98[FieldEnd]

Il separatore di campo separa il codice del campo dal valore del campo nel documento. Nota che alcuni campi hanno solo il codice del campo e non hanno né separatore di campo né valore del campo.

[Fields](../../../aspose.words.fields/) can be nested.

## Vedi anche

* Enum [VisitorAction](../../visitoraction/)
* Class [FieldStart](../../../aspose.words.fields/fieldstart/)
* Class [DocumentVisitor](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
