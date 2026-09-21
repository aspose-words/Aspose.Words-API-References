---
title: "Aspose::Words::Document::RemoveMacros method"
linktitle: "RemoveMacros"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Document::RemoveMacros method. Tar bort alla makron (VBA-projektet) samt verktygsfält och kommandotillpassningar från dokumentet i C++."
type: docs
weight: 69000
url: /sv/cpp/aspose.words/document/removemacros/
---
## Document::RemoveMacros method


Tar bort alla makron (VBA‑projektet) samt verktygsfält och kommandotillpassningar från dokumentet.

```cpp
void Aspose::Words::Document::RemoveMacros()
```

## Anmärkningar


Genom att ta bort alla makron från ett dokument kan du säkerställa att dokumentet inte innehåller några makrovirus.

## Exempel



Visar hur man tar bort alla makron från ett dokument.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Macro.docm");

ASSERT_TRUE(doc->get_HasMacros());
ASSERT_EQ(u"Project", doc->get_VbaProject()->get_Name());

// Ta bort dokumentets VBA-projekt, tillsammans med alla dess makron.
doc->RemoveMacros();

ASSERT_FALSE(doc->get_HasMacros());
ASSERT_TRUE(System::TestTools::IsNull(doc->get_VbaProject()));
```

## Se även

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
