---
title: "Aspose::Words::Properties::BuiltInDocumentProperties::get_ScaleCrop metod"
linktitle: "get_ScaleCrop"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Properties::BuiltInDocumentProperties::get_ScaleCrop metod. Anger om dokumentets miniatyrbild är beskuren eller skalad för att passa displayen i C++."
type: docs
weight: 24500
url: /sv/cpp/aspose.words.properties/builtindocumentproperties/get_scalecrop/
---
## BuiltInDocumentProperties::get_ScaleCrop method


Indikerar om dokumentets miniatyr är beskuren eller skalad för att passa displayen.

```cpp
bool Aspose::Words::Properties::BuiltInDocumentProperties::get_ScaleCrop()
```

## Anmärkningar


Aspose.Words uppdaterar inte denna egenskap.

## Exempel



Visar hur man hämtar utökade egenskaper.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Extended properties.docx");
ASSERT_TRUE(doc->get_BuiltInDocumentProperties()->get_ScaleCrop());
ASSERT_TRUE(doc->get_BuiltInDocumentProperties()->get_SharedDocument());
ASSERT_TRUE(doc->get_BuiltInDocumentProperties()->get_HyperlinksChanged());
```

## Se även

* Class [BuiltInDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
