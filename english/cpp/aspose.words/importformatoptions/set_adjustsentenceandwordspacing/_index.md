---
title: Aspose::Words::ImportFormatOptions::set_AdjustSentenceAndWordSpacing method
linktitle: set_AdjustSentenceAndWordSpacing
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::ImportFormatOptions::set_AdjustSentenceAndWordSpacing method. Sets a boolean value that specifies whether to adjust sentence and word spacing automatically. The default value is false in C++.'
type: docs
weight: 12000
url: /cpp/aspose.words/importformatoptions/set_adjustsentenceandwordspacing/
---
## ImportFormatOptions::set_AdjustSentenceAndWordSpacing method


Sets a boolean value that specifies whether to adjust sentence and word spacing automatically. The default value is **false**.

```cpp
void Aspose::Words::ImportFormatOptions::set_AdjustSentenceAndWordSpacing(bool value)
```

## Examples


Shows how to adjust sentence and word spacing automatically.

```cpp
auto srcDoc = System::MakeObject<Aspose::Words::Document>();
auto dstDoc = System::MakeObject<Aspose::Words::Document>();

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(srcDoc);
builder->Write(u"Dolor sit amet.");

builder = System::MakeObject<Aspose::Words::DocumentBuilder>(dstDoc);
builder->Write(u"Lorem ipsum.");

auto options = System::MakeObject<Aspose::Words::ImportFormatOptions>();
options->set_AdjustSentenceAndWordSpacing(true);
builder->InsertDocument(srcDoc, ImportFormatMode::UseDestinationStyles, options);

ASSERT_EQ(u"Lorem ipsum. Dolor sit amet.", dstDoc->get_FirstSection()->get_Body()->get_FirstParagraph()->GetText().Trim());
```
## See Also

* Class [ImportFormatOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
