---
title: "Aspose::Words::Fonts::FontSettings::get_DefaultInstance Methode"
linktitle: "get_DefaultInstance"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fonts::FontSettings::get_DefaultInstance Methode. Statische Standardeinstellungen für Schriften in C++."
type: docs
weight: 1000
url: /de/cpp/aspose.words.fonts/fontsettings/get_defaultinstance/
---
## FontSettings::get_DefaultInstance method


Statische Standard-Schriftarteinstellungen.

```cpp
static System::SharedPtr<Aspose::Words::Fonts::FontSettings> Aspose::Words::Fonts::FontSettings::get_DefaultInstance()
```


## Beispiele



Zeigt, wie man die Instanz der standardmäßigen Schriftarteinstellungen konfiguriert.
```cpp
// Konfigurieren Sie die Instanz der standardmäßigen Schriftarteinstellungen, um die Schriftart "Courier New" zu verwenden
// als Ersatzbackup, wenn wir versuchen, eine unbekannte Schriftart zu verwenden.
Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->get_SubstitutionSettings()->get_DefaultFontSubstitution()->set_DefaultFontName(u"Courier New");

ASSERT_TRUE(Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->get_SubstitutionSettings()->get_DefaultFontSubstitution()->get_Enabled());

auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Non-existent font");
builder->Write(u"Hello world!");

// Dieses Dokument hat keine FontSettings-Konfiguration. Wenn wir das Dokument rendern,
// wird die standardmäßige FontSettings-Instanz die fehlende Schriftart auflösen.
// Aspose.Words wird "Courier New" verwenden, um Text zu rendern, der die unbekannte Schriftart nutzt.
ASSERT_TRUE(System::TestTools::IsNull(doc->get_FontSettings()));

doc->Save(get_ArtifactsDir() + u"FontSettings.DefaultFontInstance.pdf");
```

## Siehe auch

* Class [FontSettings](../)
* Class [FontSettings](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
