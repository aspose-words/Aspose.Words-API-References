---
title: "Aspose::Words::DocumentVisitor::VisitFieldStart méthode"
linktitle: "VisitFieldStart"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::DocumentVisitor::VisitFieldStart méthode. Appelée lorsqu'un champ démarre dans le document en C++."
type: docs
weight: 23000
url: /fr/cpp/aspose.words/documentvisitor/visitfieldstart/
---
## DocumentVisitor::VisitFieldStart method


Appelé lorsqu'un champ commence dans le document.

```cpp
virtual Aspose::Words::VisitorAction Aspose::Words::DocumentVisitor::VisitFieldStart(System::SharedPtr<Aspose::Words::Fields::FieldStart> fieldStart)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| fieldStart | System::SharedPtr\<Aspose::Words::Fields::FieldStart\> | L'objet qui est visité. |

### ReturnValue

Une valeur [VisitorAction](../../visitoraction/) qui spécifie comment poursuivre l'énumération.
## Remarques


Un champ dans un document Word se compose d'un code de champ et d'une valeur de champ.

Par exemple, un champ qui affiche un numéro de page peut être représenté comme suit :

[FieldStart]PAGE[FieldSeparator]98[FieldEnd]

Le séparateur de champ sépare le code du champ de la valeur du champ dans le document. Notez que certains champs n'ont que le code du champ et ne possèdent pas de séparateur de champ ni de valeur de champ.

[Fields](../../../aspose.words.fields/) can be nested.

## Voir aussi

* Enum [VisitorAction](../../visitoraction/)
* Class [FieldStart](../../../aspose.words.fields/fieldstart/)
* Class [DocumentVisitor](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
