---
title: "Aspose::Words::Document::RemoveExternalSchemaReferences metodu"
linktitle: "RemoveExternalSchemaReferences"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Document::RemoveExternalSchemaReferences metodu. Bu belge içindeki harici XML şema referanslarını C++'ta kaldırır."
type: docs
weight: 68000
url: /tr/cpp/aspose.words/document/removeexternalschemareferences/
---
## Document::RemoveExternalSchemaReferences method


Bu belgeden harici XML şema referanslarını kaldırır.

```cpp
void Aspose::Words::Document::RemoveExternalSchemaReferences()
```


## Örnekler



Bir belgeden tüm harici XML şema referanslarını nasıl kaldıracağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"External XML schema.docx");

doc->RemoveExternalSchemaReferences();
```

## Ayrıca Bakınız

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
