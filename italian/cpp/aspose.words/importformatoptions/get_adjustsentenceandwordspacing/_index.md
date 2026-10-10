---
title: "Aspose::Words::ImportFormatOptions::get_AdjustSentenceAndWordSpacing metodo"
linktitle: "get_AdjustSentenceAndWordSpacing"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::ImportFormatOptions::get_AdjustSentenceAndWordSpacing metodo. Ottiene o imposta un valore booleano che specifica se regolare automaticamente la spaziatura di frasi e parole. Il valore predefinito è false in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words/importformatoptions/get_adjustsentenceandwordspacing/
---
## ImportFormatOptions::get_AdjustSentenceAndWordSpacing method


Ottiene o imposta un valore booleano che specifica se regolare automaticamente la spaziatura di frasi e parole. Il valore predefinito è **false**.

```cpp
bool Aspose::Words::ImportFormatOptions::get_AdjustSentenceAndWordSpacing() const
```


## Esempi



Mostra come regolare automaticamente la spaziatura di frasi e parole.
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

## Vedi anche

* Class [ImportFormatOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
