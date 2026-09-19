---
title: "Metodo Aspose::Words::Fields::FormField::Accept"
linktitle: "Accept"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Fields::FormField::Accept. Accetta un visitatore in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words.fields/formfield/accept/
---
## FormField::Accept method


Accetta un visitatore.

```cpp
bool Aspose::Words::Fields::FormField::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| visitatore | System::SharedPtr\<Aspose::Words::DocumentVisitor\> | Il visitatore che visiterà il nodo. |

### ReturnValue

**false** if the visitor requested the enumeration to stop.
## Note


Chiama [VisitFormField()](../../../aspose.words/documentvisitor/visitformfield/).

Per ulteriori informazioni vedere il pattern di progettazione Visitor.

## Vedi anche

* Class [DocumentVisitor](../../../aspose.words/documentvisitor/)
* Class [FormField](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
