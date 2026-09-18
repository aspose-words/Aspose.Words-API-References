---
title: "Aspose::Words::ImportFormatOptions::get_AdjustSentenceAndWordSpacing Methode"
linktitle: "get_AdjustSentenceAndWordSpacing"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::ImportFormatOptions::get_AdjustSentenceAndWordSpacing Methode. Gibt einen booleschen Wert zurück oder legt ihn fest, der angibt, ob Satz- und Wortabstände automatisch angepasst werden sollen. Der Standardwert ist false in C++."
type: docs
weight: 3000
url: /de/cpp/aspose.words/importformatoptions/get_adjustsentenceandwordspacing/
---
## ImportFormatOptions::get_AdjustSentenceAndWordSpacing method


Liest oder setzt einen booleschen Wert, der angibt, ob Satz- und Wortabstände automatisch angepasst werden sollen. Der Standardwert ist **false**.

```cpp
bool Aspose::Words::ImportFormatOptions::get_AdjustSentenceAndWordSpacing() const
```


## Beispiele



Zeigt, wie Satz- und Wortabstände automatisch angepasst werden.
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

## Siehe auch

* Class [ImportFormatOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
