---
title: "Aspose::Words::ControlChar::Cr metod"
linktitle: "Cr"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::ControlChar::Cr metod. Vagnreturtecken: \"\\x000d\" eller \"\\r\". Samma som ParagraphBreak i C++."
type: docs
weight: 3000
url: /sv/cpp/aspose.words/controlchar/cr/
---
## ControlChar::Cr method


Vagnreturtecken: "\x000d" eller "\r". Samma som [ParagraphBreak](../paragraphbreak/).

```cpp
static System::String & Aspose::Words::ControlChar::Cr()
```


## Exempel



Visar hur man använder kontrolltecken.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Infoga stycken med text med DocumentBuilder.
builder->Writeln(u"Hello world!");
builder->Writeln(u"Hello again!");

// Att konvertera dokumentet till textform avslöjar att kontrolltecken
// representerar några av dokumentets strukturella element, såsom sidbrytningar.
ASSERT_EQ(System::String::Format(u"Hello world!{0}", Aspose::Words::ControlChar::Cr()) + System::String::Format(u"Hello again!{0}", Aspose::Words::ControlChar::Cr()) + Aspose::Words::ControlChar::PageBreak(), doc->GetText());

// När man konverterar ett dokument till strängform,
// kan vi utelämna vissa kontrolltecken med Trim‑metoden.
ASSERT_EQ(System::String::Format(u"Hello world!{0}", Aspose::Words::ControlChar::Cr()) + u"Hello again!", doc->GetText().Trim());
```

## Se även

* Class [ControlChar](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
