---
title: "Aspose::Words::DocumentVisitor::VisitFieldSeparator méthode"
linktitle: "VisitFieldSeparator"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::DocumentVisitor::VisitFieldSeparator méthode. Appelée lorsqu'un séparateur de champ est rencontré dans le document en C++."
type: docs
weight: 22000
url: /fr/cpp/aspose.words/documentvisitor/visitfieldseparator/
---
## DocumentVisitor::VisitFieldSeparator method


Appelé lorsqu'un séparateur de champ est rencontré dans le document.

```cpp
virtual Aspose::Words::VisitorAction Aspose::Words::DocumentVisitor::VisitFieldSeparator(System::SharedPtr<Aspose::Words::Fields::FieldSeparator> fieldSeparator)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| fieldSeparator | System::SharedPtr\<Aspose::Words::Fields::FieldSeparator\> | L'objet qui est visité. |

### ReturnValue

Une valeur [VisitorAction](../../visitoraction/) qui spécifie comment poursuivre l'énumération.
## Remarques


Le séparateur de champ sépare le code du champ de la valeur du champ dans le document. Notez que certains champs n'ont que le code du champ et ne possèdent pas de séparateur de champ ni de valeur de champ.

Pour plus d'informations, voir [VisitFieldStart()](../visitfieldstart/)

## Voir aussi

* Enum [VisitorAction](../../visitoraction/)
* Class [FieldSeparator](../../../aspose.words.fields/fieldseparator/)
* Class [DocumentVisitor](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
