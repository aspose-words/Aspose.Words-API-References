---
title: "Aspose::Words::Document::RemoveExternalSchemaReferences metod"
linktitle: "RemoveExternalSchemaReferences"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Document::RemoveExternalSchemaReferences metod. Tar bort externa XML-schemareferenser från detta dokument i C++."
type: docs
weight: 68000
url: /sv/cpp/aspose.words/document/removeexternalschemareferences/
---
## Document::RemoveExternalSchemaReferences method


Tar bort externa XML‑schemareferenser från detta dokument.

```cpp
void Aspose::Words::Document::RemoveExternalSchemaReferences()
```


## Exempel



Visar hur man tar bort alla externa XML-schemareferenser från ett dokument.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"External XML schema.docx");

doc->RemoveExternalSchemaReferences();
```

## Se även

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
