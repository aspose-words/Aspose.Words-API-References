---
title: "Aspose::Words::Fonts::FontSourceBase::get_Type método"
linktitle: "get_Type"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Fonts::FontSourceBase::get_Type método. Devuelve el tipo de la fuente de fuentes en C++."
type: docs
weight: 3000
url: /es/cpp/aspose.words.fonts/fontsourcebase/get_type/
---
## FontSourceBase::get_Type method


Devuelve el tipo de la fuente de fuentes.

```cpp
virtual Aspose::Words::Fonts::FontSourceType Aspose::Words::Fonts::FontSourceBase::get_Type()=0
```


## Ejemplos



Muestra cómo usar un archivo de fuente en el sistema de archivos local como origen de fuente.
```cpp
auto fileFontSource = System::MakeObject<Aspose::Words::Fonts::FileFontSource>(get_MyDir() + u"Alte DIN 1451 Mittelschrift.ttf", 0);

auto doc = System::MakeObject<Aspose::Words::Document>();
doc->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());
doc->get_FontSettings()->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({fileFontSource}));

ASSERT_EQ(get_MyDir() + u"Alte DIN 1451 Mittelschrift.ttf", fileFontSource->get_FilePath());
ASSERT_EQ(Aspose::Words::Fonts::FontSourceType::FontFile, fileFontSource->get_Type());
ASSERT_EQ(0, fileFontSource->get_Priority());
```

## Ver también

* Enum [FontSourceType](../../fontsourcetype/)
* Class [FontSourceBase](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
