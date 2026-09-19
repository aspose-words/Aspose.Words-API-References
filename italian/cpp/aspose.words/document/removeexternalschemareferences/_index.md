---
title: "Aspose::Words::Document::RemoveExternalSchemaReferences method"
linktitle: "RemoveExternalSchemaReferences"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Document::RemoveExternalSchemaReferences method. Rimuove i riferimenti a schemi XML esterni da questo documento in C++."
type: docs
weight: 68000
url: /it/cpp/aspose.words/document/removeexternalschemareferences/
---
## Document::RemoveExternalSchemaReferences method


Rimuove i riferimenti a schemi XML esterni da questo documento.

```cpp
void Aspose::Words::Document::RemoveExternalSchemaReferences()
```


## Esempi



Mostra come rimuovere tutti i riferimenti a schemi XML esterni da un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"External XML schema.docx");

doc->RemoveExternalSchemaReferences();
```

## Vedi anche

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
