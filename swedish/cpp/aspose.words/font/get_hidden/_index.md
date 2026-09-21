---
title: "Aspose::Words::Font::get_Hidden metod"
linktitle: "get_Hidden"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Font::get_Hidden metod. Sant om teckensnittet är formaterat som dold text i C++."
type: docs
weight: 16000
url: /sv/cpp/aspose.words/font/get_hidden/
---
## Font::get_Hidden method


Sant om teckensnittet är formaterat som dold text.

```cpp
bool Aspose::Words::Font::get_Hidden()
```


## Exempel



Visar hur man skapar en sekvens av dold text.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// När den dolda flaggan är satt till true kommer all text som vi skapar med detta Font-objekt att vara osynlig i dokumentet.
// Vi kommer inte att se eller markera dold text om vi inte aktiverar alternativet "Hidden text".
// finns i Microsoft Word via "File" -> "Options" -> "Display". Texten kommer fortfarande att finnas där,
// och vi kommer att kunna komma åt denna text programmässigt.
// Det rekommenderas inte att använda denna metod för att dölja känslig information.
builder->get_Font()->set_Hidden(true);
builder->get_Font()->set_Size(36);

builder->Writeln(u"This text will not be visible in the document.");

doc->Save(get_ArtifactsDir() + u"Font.Hidden.docx");
```

## Se även

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
