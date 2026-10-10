---
title: "Aspose::Words::Properties::BuiltInDocumentProperties::get_ScaleCrop Methode"
linktitle: "get_ScaleCrop"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Properties::BuiltInDocumentProperties::get_ScaleCrop Methode. Gibt an, ob das Dokumenten‑Miniaturbild beschnitten oder skaliert ist, um auf die Anzeige zu passen, in C++."
type: docs
weight: 24500
url: /de/cpp/aspose.words.properties/builtindocumentproperties/get_scalecrop/
---
## BuiltInDocumentProperties::get_ScaleCrop method


Gibt an, ob das Dokumentenvorschaubild beschnitten oder skaliert wird, um in die Anzeige zu passen.

```cpp
bool Aspose::Words::Properties::BuiltInDocumentProperties::get_ScaleCrop()
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
