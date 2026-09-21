---
title: "Aspose::Words::Properties::BuiltInDocumentProperties::get_HyperlinksChanged metod"
linktitle: "get_HyperlinksChanged"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Properties::BuiltInDocumentProperties::get_HyperlinksChanged metod. Anger om hyperlänkar i ett dokument har ändrats i C++."
type: docs
weight: 13500
url: /sv/cpp/aspose.words.properties/builtindocumentproperties/get_hyperlinkschanged/
---
## BuiltInDocumentProperties::get_HyperlinksChanged method


Indikerar om hyperlänkar i ett dokument har ändrats.

```cpp
bool Aspose::Words::Properties::BuiltInDocumentProperties::get_HyperlinksChanged()
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
