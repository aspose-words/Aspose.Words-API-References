---
title: "Aspose::Words::ControlChar::Cr Methode"
linktitle: "Cr"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::ControlChar::Cr Methode. Wagenrücklauf Zeichen: \"\\x000d\" oder \"\\r\". Gleich wie ParagraphBreak in C++."
type: docs
weight: 3000
url: /de/cpp/aspose.words/controlchar/cr/
---
## ControlChar::Cr method


Wagenrücklauf Zeichen: "\x000d" oder "\r". Gleich wie [ParagraphBreak](../paragraphbreak/).

```cpp
static System::String & Aspose::Words::ControlChar::Cr()
```


## Beispiele



Zeigt, wie Steuerzeichen verwendet werden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Fügt Absätze mit Text mittels DocumentBuilder ein.
builder->Writeln(u"Hello world!");
builder->Writeln(u"Hello again!");

// Das Konvertieren des Dokuments in Textform zeigt, dass Steuerzeichen
// einige der strukturellen Elemente des Dokuments darstellen, wie z. B. Seitenumbrüche.
ASSERT_EQ(System::String::Format(u"Hello world!{0}", Aspose::Words::ControlChar::Cr()) + System::String::Format(u"Hello again!{0}", Aspose::Words::ControlChar::Cr()) + Aspose::Words::ControlChar::PageBreak(), doc->GetText());

// Beim Konvertieren eines Dokuments in Zeichenkettenform,
// können wir einige Steuerzeichen mit der Trim-Methode weglassen.
ASSERT_EQ(System::String::Format(u"Hello world!{0}", Aspose::Words::ControlChar::Cr()) + u"Hello again!", doc->GetText().Trim());
```

## Siehe auch

* Class [ControlChar](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
