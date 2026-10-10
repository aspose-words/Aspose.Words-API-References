---
title: "Aspose::Words::Fonts::FontSourceBase::get_Priority método"
linktitle: "get_Priority"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Fonts::FontSourceBase::get_Priority método. Devuelve la prioridad de la fuente en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words.fonts/fontsourcebase/get_priority/
---
## FontSourceBase::get_Priority method


Devuelve la prioridad de la fuente de fuentes.

```cpp
int32_t Aspose::Words::Fonts::FontSourceBase::get_Priority() const
```

## Observaciones


Este valor se usa cuando hay fuentes con el mismo nombre de familia y estilo en diferentes fuentes tipográficas. En este caso Aspose.Words selecciona la fuente de la fuente con el valor de prioridad más alto.

El valor predeterminado es 0.

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

* Class [FontSourceBase](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
