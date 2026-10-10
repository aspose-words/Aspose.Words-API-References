---
title: "Aspose::Words::Properties::BuiltInDocumentProperties::get_HyperlinksChanged Methode"
linktitle: "get_HyperlinksChanged"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Properties::BuiltInDocumentProperties::get_HyperlinksChanged Methode. Gibt an, ob Hyperlinks in einem Dokument in C++ geändert wurden."
type: docs
weight: 13500
url: /de/cpp/aspose.words.properties/builtindocumentproperties/get_hyperlinkschanged/
---
## BuiltInDocumentProperties::get_HyperlinksChanged method


Gibt an, ob Hyperlinks in einem Dokument geändert wurden.

```cpp
bool Aspose::Words::Properties::BuiltInDocumentProperties::get_HyperlinksChanged()
```

## Hinweise


Aspose.Words aktualisiert diese Eigenschaft nicht.

## Beispiele



Zeigt, wie erweiterte Eigenschaften abgerufen werden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Extended properties.docx");
ASSERT_TRUE(doc->get_BuiltInDocumentProperties()->get_ScaleCrop());
ASSERT_TRUE(doc->get_BuiltInDocumentProperties()->get_SharedDocument());
ASSERT_TRUE(doc->get_BuiltInDocumentProperties()->get_HyperlinksChanged());
```

## Siehe auch

* Class [BuiltInDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
