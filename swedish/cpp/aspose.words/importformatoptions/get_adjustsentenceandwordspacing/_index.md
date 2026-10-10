---
title: "Aspose::Words::ImportFormatOptions::get_AdjustSentenceAndWordSpacing metod"
linktitle: "get_AdjustSentenceAndWordSpacing"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::ImportFormatOptions::get_AdjustSentenceAndWordSpacing metod. Hämtar eller anger ett booleskt värde som specificerar om menings- och ordavstånd ska justeras automatiskt. Standardvärdet är false i C++."
type: docs
weight: 3000
url: /sv/cpp/aspose.words/importformatoptions/get_adjustsentenceandwordspacing/
---
## ImportFormatOptions::get_AdjustSentenceAndWordSpacing method


Hämtar eller anger ett booleskt värde som specificerar om menings- och ordavstånd ska justeras automatiskt. Standardvärdet är **false**.

```cpp
bool Aspose::Words::ImportFormatOptions::get_AdjustSentenceAndWordSpacing() const
```


## Exempel



Visar hur man justerar mening- och ordavstånd automatiskt.
```cpp
auto srcDoc = System::MakeObject<Aspose::Words::Document>();
auto dstDoc = System::MakeObject<Aspose::Words::Document>();

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(srcDoc);
builder->Write(u"Dolor sit amet.");

builder = System::MakeObject<Aspose::Words::DocumentBuilder>(dstDoc);
builder->Write(u"Lorem ipsum.");

auto options = System::MakeObject<Aspose::Words::ImportFormatOptions>();
options->set_AdjustSentenceAndWordSpacing(true);
builder->InsertDocument(srcDoc, Aspose::Words::ImportFormatMode::UseDestinationStyles, options);

ASSERT_EQ(u"Lorem ipsum. Dolor sit amet.", dstDoc->get_FirstSection()->get_Body()->get_FirstParagraph()->GetText().Trim());
```

## Se även

* Class [ImportFormatOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
