---
title: "Aspose::Words::Fonts::FontSettings::get_DefaultInstance method"
linktitle: "get_DefaultInstance"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fonts::FontSettings::get_DefaultInstance method. Impostazioni predefinite statiche dei caratteri in C++."
type: docs
weight: 1000
url: /it/cpp/aspose.words.fonts/fontsettings/get_defaultinstance/
---
## FontSettings::get_DefaultInstance method


Impostazioni dei caratteri predefinite statiche.

```cpp
static System::SharedPtr<Aspose::Words::Fonts::FontSettings> Aspose::Words::Fonts::FontSettings::get_DefaultInstance()
```


## Esempi



Mostra come configurare l'istanza delle impostazioni predefinite dei caratteri.
```cpp
// Configura l'istanza delle impostazioni predefinite dei caratteri per utilizzare il carattere "Courier New"
// come sostituto di backup quando tentiamo di utilizzare un carattere sconosciuto.
Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->get_SubstitutionSettings()->get_DefaultFontSubstitution()->set_DefaultFontName(u"Courier New");

ASSERT_TRUE(Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->get_SubstitutionSettings()->get_DefaultFontSubstitution()->get_Enabled());

auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Non-existent font");
builder->Write(u"Hello world!");

// Questo documento non ha una configurazione di FontSettings. Quando renderizziamo il documento,
// l'istanza predefinita di FontSettings risolverà il carattere mancante.
// Aspose.Words utilizzerà "Courier New" per renderizzare il testo che utilizza il carattere sconosciuto.
ASSERT_TRUE(System::TestTools::IsNull(doc->get_FontSettings()));

doc->Save(get_ArtifactsDir() + u"FontSettings.DefaultFontInstance.pdf");
```

## Vedi anche

* Class [FontSettings](../)
* Class [FontSettings](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
