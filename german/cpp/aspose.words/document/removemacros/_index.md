---
title: "Aspose::Words::Document::RemoveMacros Methode"
linktitle: "RemoveMacros"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Document::RemoveMacros Methode. Entfernt alle Makros (das VBA-Projekt) sowie Symbolleisten und Befehlsanpassungen aus dem Dokument in C++."
type: docs
weight: 69000
url: /de/cpp/aspose.words/document/removemacros/
---
## Document::RemoveMacros method


Entfernt alle Makros (das VBA‑Projekt) sowie Toolbars und Befehlsanpassungen aus dem Dokument.

```cpp
void Aspose::Words::Document::RemoveMacros()
```

## Hinweise


Durch das Entfernen aller Makros aus einem Dokument können Sie sicherstellen, dass das Dokument keine Makroviren enthält.

## Beispiele



Zeigt, wie man alle Makros aus einem Dokument entfernt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Macro.docm");

ASSERT_TRUE(doc->get_HasMacros());
ASSERT_EQ(u"Project", doc->get_VbaProject()->get_Name());

// Entfernt das VBA-Projekt des Dokuments sowie alle zugehörigen Makros.
doc->RemoveMacros();

ASSERT_FALSE(doc->get_HasMacros());
ASSERT_TRUE(System::TestTools::IsNull(doc->get_VbaProject()));
```

## Siehe auch

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
