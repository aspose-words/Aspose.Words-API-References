---
title: Aspose::Words::Fonts::FontSettings::get_DefaultInstance method
linktitle: get_DefaultInstance
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fonts::FontSettings::get_DefaultInstance method. Static default font settings in C++.'
type: docs
weight: 1000
url: /cpp/aspose.words.fonts/fontsettings/get_defaultinstance/
---
## FontSettings::get_DefaultInstance method


Static default font settings.

```cpp
static System::SharedPtr<Aspose::Words::Fonts::FontSettings> Aspose::Words::Fonts::FontSettings::get_DefaultInstance()
```


## Examples



Shows how to configure the default font settings instance. 
```cpp
// Configure the default font settings instance to use the "Courier New" font
// as a backup substitute when we attempt to use an unknown font.
Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->get_SubstitutionSettings()->get_DefaultFontSubstitution()->set_DefaultFontName(u"Courier New");

ASSERT_TRUE(Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->get_SubstitutionSettings()->get_DefaultFontSubstitution()->get_Enabled());

auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Non-existent font");
builder->Write(u"Hello world!");

// This document does not have a FontSettings configuration. When we render the document,
// the default FontSettings instance will resolve the missing font.
// Aspose.Words will use "Courier New" to render text that uses the unknown font.
ASSERT_TRUE(System::TestTools::IsNull(doc->get_FontSettings()));

doc->Save(get_ArtifactsDir() + u"FontSettings.DefaultFontInstance.pdf");
```

## See Also

* Class [FontSettings](../)
* Class [FontSettings](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
