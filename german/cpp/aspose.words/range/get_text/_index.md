---
title: "Aspose::Words::Range::get_Text Methode"
linktitle: "get_Text"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Range::get_Text Methode. Gibt den Text des Bereichs in C++ zurück."
type: docs
weight: 8000
url: /de/cpp/aspose.words/range/get_text/
---
## Range::get_Text method


Ruft den Text des Bereichs ab.

```cpp
System::String Aspose::Words::Range::get_Text()
```

## Hinweise


Der zurückgegebene String enthält alle Steuer- und Sonderzeichen wie in [ControlChar](../../controlchar/) beschrieben.

## Beispiele



Zeigt, wie man den Textinhalt aller Knoten abruft, die von einem Bereich abgedeckt werden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Hello world!");

ASSERT_EQ(u"Hello world!", doc->get_Range()->get_Text().Trim());
```

## Siehe auch

* Class [Range](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
