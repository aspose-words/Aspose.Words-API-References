---
title: "Aspose::Words::Document::RemoveExternalSchemaReferences Methode"
linktitle: "RemoveExternalSchemaReferences"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Document::RemoveExternalSchemaReferences Methode. Entfernt externe XML‑Schema‑Verweise aus diesem Dokument in C++."
type: docs
weight: 68000
url: /de/cpp/aspose.words/document/removeexternalschemareferences/
---
## Document::RemoveExternalSchemaReferences method


Entfernt externe XML‑Schemainreferenzen aus diesem Dokument.

```cpp
void Aspose::Words::Document::RemoveExternalSchemaReferences()
```


## Beispiele



Zeigt, wie alle externen XML‑Schema‑Verweise aus einem Dokument entfernt werden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"External XML schema.docx");

doc->RemoveExternalSchemaReferences();
```

## Siehe auch

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
