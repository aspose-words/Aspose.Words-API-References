---
title: "Aspose::Words::DocumentVisitor::VisitFieldSeparator method"
linktitle: "VisitFieldSeparator"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::DocumentVisitor::VisitFieldSeparator method. Chiamato quando viene incontrato un separatore di campo nel documento in C++."
type: docs
weight: 22000
url: /it/cpp/aspose.words/documentvisitor/visitfieldseparator/
---
## DocumentVisitor::VisitFieldSeparator method


Chiamato quando viene incontrato un separatore di campo nel documento.

```cpp
virtual Aspose::Words::VisitorAction Aspose::Words::DocumentVisitor::VisitFieldSeparator(System::SharedPtr<Aspose::Words::Fields::FieldSeparator> fieldSeparator)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fieldSeparator | System::SharedPtr\<Aspose::Words::Fields::FieldSeparator\> | L'oggetto che viene visitato. |

### ReturnValue

Un valore [VisitorAction](../../visitoraction/) che specifica come continuare l'enumerazione.
## Note


Il separatore di campo separa il codice del campo dal valore del campo nel documento. Nota che alcuni campi hanno solo il codice del campo e non hanno né separatore di campo né valore del campo.

Per ulteriori informazioni vedere [VisitFieldStart()](../visitfieldstart/)

## Vedi anche

* Enum [VisitorAction](../../visitoraction/)
* Class [FieldSeparator](../../../aspose.words.fields/fieldseparator/)
* Class [DocumentVisitor](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
