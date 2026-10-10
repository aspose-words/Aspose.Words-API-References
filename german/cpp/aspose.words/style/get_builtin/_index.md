---
title: "Aspose::Words::Style::get_BuiltIn Methode"
linktitle: "get_BuiltIn"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Style::get_BuiltIn Methode. True, wenn dieser Stil einer der integrierten Stile in MS Word in C++ ist."
type: docs
weight: 6000
url: /de/cpp/aspose.words/style/get_builtin/
---
## Style::get_BuiltIn method


Wahr, wenn dieser Stil einer der integrierten Stile in MS Word ist.

```cpp
bool Aspose::Words::Style::get_BuiltIn()
```


## Beispiele



Zeigt, wie man benutzerdefinierte Stile von integrierten Stilen unterscheidet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Wenn wir ein Dokument mit Microsoft Word oder programmgesteuert mit Aspose.Words erstellen,
// wird das Dokument mit einer Sammlung von Stilen geliefert, die auf den Text angewendet werden können, um das Aussehen zu ändern.
// Wir können auf diese integrierten Stile über die "Styles"‑Sammlung des Dokuments zugreifen.
// Alle diese Stile haben das Flag "BuiltIn" auf "true" gesetzt.
System::SharedPtr<Aspose::Words::Style> style = doc->get_Styles()->idx_get(u"Emphasis");

ASSERT_TRUE(style->get_BuiltIn());

// Erstellen Sie einen benutzerdefinierten Stil und fügen Sie ihn der Sammlung hinzu.
// Benutzerdefinierte Stile wie dieser haben das Flag "BuiltIn" auf "false" gesetzt.
style = doc->get_Styles()->Add(Aspose::Words::StyleType::Character, u"MyStyle");
style->get_Font()->set_Color(System::Drawing::Color::get_Navy());
style->get_Font()->set_Name(u"Courier New");

ASSERT_FALSE(style->get_BuiltIn());
```

## Siehe auch

* Class [Style](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
