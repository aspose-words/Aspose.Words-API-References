---
title: Aspose::Words::Properties::BuiltInDocumentProperties::get_SharedDocument method
linktitle: get_SharedDocument
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Properties::BuiltInDocumentProperties::get_SharedDocument method. Indicates whether the document is a shared document in C++.'
type: docs
weight: 25500
url: /cpp/aspose.words.properties/builtindocumentproperties/get_shareddocument/
---
## BuiltInDocumentProperties::get_SharedDocument method


Indicates whether the document is a shared document.

```cpp
bool Aspose::Words::Properties::BuiltInDocumentProperties::get_SharedDocument()
```

## Remarks


Aspose.Words does not update this property.

## Examples



Shows how to get extended properties. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Extended properties.docx");
ASSERT_TRUE(doc->get_BuiltInDocumentProperties()->get_ScaleCrop());
ASSERT_TRUE(doc->get_BuiltInDocumentProperties()->get_SharedDocument());
ASSERT_TRUE(doc->get_BuiltInDocumentProperties()->get_HyperlinksChanged());
```

## See Also

* Class [BuiltInDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
