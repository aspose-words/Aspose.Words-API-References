---
title: "Aspose::Words::PageSetup::get_TextOrientation metod"
linktitle: "get_TextOrientation"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::PageSetup::get_TextOrientation metod. Tillåter att ange TextOrientation för hela sidan. Standardvärdet är Horizontal i C++."
type: docs
weight: 45000
url: /sv/cpp/aspose.words/pagesetup/get_textorientation/
---
## PageSetup::get_TextOrientation method


Tillåter att ange [TextOrientation](./) för hela sidan. Standardvärdet är [Horizontal](../../textorientation/)

```cpp
Aspose::Words::TextOrientation Aspose::Words::PageSetup::get_TextOrientation()
```


## Exempel



Visar hur man ställer in textorientering.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

// Ställ in egenskapen "TextOrientation" till "TextOrientation.Upward" för att rotera all text 90 grader
// till höger så att all vänster‑till‑höger-text nu går uppifrån och ner.
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();
pageSetup->set_TextOrientation(Aspose::Words::TextOrientation::Upward);

doc->Save(get_ArtifactsDir() + u"PageSetup.SetTextOrientation.docx");
```

## Se även

* Enum [TextOrientation](../../textorientation/)
* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
