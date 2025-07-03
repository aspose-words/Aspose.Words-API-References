---
title: Aspose::Words::Font::get_Subscript method
linktitle: get_Subscript
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Font::get_Subscript method. True if the font is formatted as subscript in C++.'
type: docs
weight: 45000
url: /cpp/aspose.words/font/get_subscript/
---
## Font::get_Subscript method


True if the font is formatted as subscript.

```cpp
bool Aspose::Words::Font::get_Subscript()
```


## Examples



Shows how to format text to offset its position. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto para = System::ExplicitCast<Aspose::Words::Paragraph>(doc->GetChild(Aspose::Words::NodeType::Paragraph, 0, true));

// Raise this run of text 5 points above the baseline.
auto run = System::MakeObject<Aspose::Words::Run>(doc, u"Raised text. ");
run->get_Font()->set_Position(5);
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

// Lower this run of text 10 points below the baseline.
run = System::MakeObject<Aspose::Words::Run>(doc, u"Lowered text. ");
run->get_Font()->set_Position(-10);
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

// Add a run of normal text.
run = System::MakeObject<Aspose::Words::Run>(doc, u"Text in its default position. ");
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

// Add a run of text that appears as subscript.
run = System::MakeObject<Aspose::Words::Run>(doc, u"Subscript. ");
run->get_Font()->set_Subscript(true);
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

// Add a run of text that appears as superscript.
run = System::MakeObject<Aspose::Words::Run>(doc, u"Superscript.");
run->get_Font()->set_Superscript(true);
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

doc->Save(get_ArtifactsDir() + u"Font.PositionSubscript.docx");
```

## See Also

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
