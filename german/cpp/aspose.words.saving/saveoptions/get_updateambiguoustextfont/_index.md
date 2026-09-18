---
title: "Aspose::Words::Saving::SaveOptions::get_UpdateAmbiguousTextFont Methode"
linktitle: "get_UpdateAmbiguousTextFont"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::SaveOptions::get_UpdateAmbiguousTextFont Methode. Bestimmt, ob die Schriftattribute gemäß dem verwendeten Zeichencode in C++ geändert werden."
type: docs
weight: 15500
url: /de/cpp/aspose.words.saving/saveoptions/get_updateambiguoustextfont/
---
## SaveOptions::get_UpdateAmbiguousTextFont method


Bestimmt, ob die Schriftattribute entsprechend dem verwendeten Zeichencode geändert werden.

```cpp
bool Aspose::Words::Saving::SaveOptions::get_UpdateAmbiguousTextFont() const
```


## Beispiele



Zeigt, wie die Schriftart aktualisiert wird, um dem verwendeten Zeichencode zu entsprechen.
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

## Siehe auch

* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
