---
title: Aspose::Words::Saving::SaveOptions::get_UpdateAmbiguousTextFont method
linktitle: get_UpdateAmbiguousTextFont
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::SaveOptions::get_UpdateAmbiguousTextFont method. Determines whether the font attributes will be changed according to the character code being used in C++.'
type: docs
weight: 15500
url: /cpp/aspose.words.saving/saveoptions/get_updateambiguoustextfont/
---
## SaveOptions::get_UpdateAmbiguousTextFont method


Determines whether the font attributes will be changed according to the character code being used.

```cpp
bool Aspose::Words::Saving::SaveOptions::get_UpdateAmbiguousTextFont() const
```


## Examples



Shows how to update the font to match the character code being used. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Special symbol.docx");
System::SharedPtr<Aspose::Words::Run> run = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0);
std::cout << run->get_Text() << std::endl;
// ฿
std::cout << run->get_Font()->get_Name() << std::endl;
// Arial

auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>();
saveOptions->set_UpdateAmbiguousTextFont(true);
doc->Save(get_ArtifactsDir() + u"OoxmlSaveOptions.UpdateAmbiguousTextFont.docx", saveOptions);

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OoxmlSaveOptions.UpdateAmbiguousTextFont.docx");
run = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0);
std::cout << run->get_Text() << std::endl;
// ฿
std::cout << run->get_Font()->get_Name() << std::endl;
// Angsana New
```

## See Also

* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
