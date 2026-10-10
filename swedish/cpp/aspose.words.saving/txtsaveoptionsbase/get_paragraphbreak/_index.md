---
title: "Aspose::Words::Saving::TxtSaveOptionsBase::get_ParagraphBreak-metod"
linktitle: "get_ParagraphBreak"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::TxtSaveOptionsBase::get_ParagraphBreak-metod. Anger strängen som ska användas som styckebrytning vid export i textformat i C++."
type: docs
weight: 6000
url: /sv/cpp/aspose.words.saving/txtsaveoptionsbase/get_paragraphbreak/
---
## TxtSaveOptionsBase::get_ParagraphBreak method


Anger strängen som ska användas som styckebrytning vid export i textformat.

```cpp
System::String Aspose::Words::Saving::TxtSaveOptionsBase::get_ParagraphBreak() const
```

## Anmärkningar


Standardvärdet är [CrLf](../../../aspose.words/controlchar/crlf/).

## Exempel



Visar hur man sparar ett .txt-dokument med en anpassad styckebrytning.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Paragraph 1.");
builder->Writeln(u"Paragraph 2.");
builder->Write(u"Paragraph 3.");

// Skapa ett \"TxtSaveOptions\"-objekt, som vi kan skicka till dokumentets \"Save\"-metod
// för att ändra hur vi sparar dokumentet som ren text.
auto txtSaveOptions = System::MakeObject<Aspose::Words::Saving::TxtSaveOptions>();

ASSERT_EQ(Aspose::Words::SaveFormat::Text, txtSaveOptions->get_SaveFormat());

// Ställ in \"ParagraphBreak\" till ett anpassat värde som vi vill placera i slutet av varje stycke.
txtSaveOptions->set_ParagraphBreak(u" End of paragraph.\n\n\t");

doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.ParagraphBreak.txt", txtSaveOptions);

System::String docText = System::IO::File::ReadAllText(get_ArtifactsDir() + u"TxtSaveOptions.ParagraphBreak.txt");

ASSERT_EQ(System::String(u"Paragraph 1. End of paragraph.\n\n\t") + u"Paragraph 2. End of paragraph.\n\n\t" + u"Paragraph 3. End of paragraph.\n\n\t", docText);
```

## Se även

* Class [TxtSaveOptionsBase](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
