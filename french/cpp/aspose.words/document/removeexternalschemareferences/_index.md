---
title: "Aspose::Words::Document::RemoveExternalSchemaReferences méthode"
linktitle: "RemoveExternalSchemaReferences"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Document::RemoveExternalSchemaReferences méthode. Supprime les références de schéma XML externes de ce document en C++."
type: docs
weight: 68000
url: /fr/cpp/aspose.words/document/removeexternalschemareferences/
---
## Document::RemoveExternalSchemaReferences method


Supprime les références de schémas XML externes de ce document.

```cpp
void Aspose::Words::Document::RemoveExternalSchemaReferences()
```


## Exemples



Montre comment supprimer toutes les références de schéma XML externes d'un document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"External XML schema.docx");

doc->RemoveExternalSchemaReferences();
```

## Voir aussi

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
