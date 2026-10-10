---
title: "Aspose::Words::Document::get_VersionsCount metod"
linktitle: "get_VersionsCount"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Document::get_VersionsCount metod. Hämtar antalet dokumentversioner som lagrades i DOC-dokumentet i C++."
type: docs
weight: 57000
url: /sv/cpp/aspose.words/document/get_versionscount/
---
## Document::get_VersionsCount method


Hämtar antalet dokumentversioner som lagrades i DOC‑dokumentet.

```cpp
int32_t Aspose::Words::Document::get_VersionsCount()
```

## Anmärkningar


Versioner i Microsoft Word nås via menyn Arkiv/Versioner. Microsoft Word stöder versioner endast för DOC-filer.

Denna egenskap möjliggör att upptäcka om det fanns dokumentversioner lagrade i detta dokument innan det öppnades i Aspose.Words. Aspose.Words tillhandahåller inget annat stöd för dokumentversioner. Om du sparar detta dokument med Aspose.Words kommer dokumentet att sparas utan versioner.

## Exempel



Visar hur man arbetar med versionsräknarfunktionen i äldre Microsoft Word-dokument.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Versions.doc");

// Vi kan läsa denna egenskap i ett dokument, men vi kan inte bevara den vid sparande.
ASSERT_EQ(4, doc->get_VersionsCount());

doc->Save(get_ArtifactsDir() + u"Document.VersionsCount.doc");
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Document.VersionsCount.doc");

ASSERT_EQ(0, doc->get_VersionsCount());
```

## Se även

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
