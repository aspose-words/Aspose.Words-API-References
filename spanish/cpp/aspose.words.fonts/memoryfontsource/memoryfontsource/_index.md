---
title: "Aspose::Words::Fonts::MemoryFontSource::MemoryFontSource constructor"
linktitle: "MemoryFontSource"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Fonts::MemoryFontSource::MemoryFontSource constructor. Ctor en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words.fonts/memoryfontsource/memoryfontsource/
---
## MemoryFontSource::MemoryFontSource(const System::ArrayPtr\<uint8_t\>\&) constructor


Ctor.

```cpp
Aspose::Words::Fonts::MemoryFontSource::MemoryFontSource(const System::ArrayPtr<uint8_t> &fontData)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| fontData | const System::ArrayPtr\<uint8_t\>\& | Datos de fuente binarios. |

## Ejemplos



Muestra cómo usar una matriz de bytes con datos de un archivo de fuente como una fuente.
```cpp
System::ArrayPtr<uint8_t> fontBytes = System::IO::File::ReadAllBytes(get_MyDir() + u"Alte DIN 1451 Mittelschrift.ttf");
auto memoryFontSource = System::MakeObject<Aspose::Words::Fonts::MemoryFontSource>(fontBytes, 0);

auto doc = System::MakeObject<Aspose::Words::Document>();
doc->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());
doc->get_FontSettings()->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({memoryFontSource}));

ASSERT_EQ(Aspose::Words::Fonts::FontSourceType::MemoryFont, memoryFontSource->get_Type());
ASSERT_EQ(0, memoryFontSource->get_Priority());
```

## Ver también

* Class [MemoryFontSource](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
## MemoryFontSource::MemoryFontSource(const System::ArrayPtr\<uint8_t\>\&, int32_t) constructor


Ctor.

```cpp
Aspose::Words::Fonts::MemoryFontSource::MemoryFontSource(const System::ArrayPtr<uint8_t> &fontData, int32_t priority)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| fontData | const System::ArrayPtr\<uint8_t\>\& | Datos de fuente binarios. |
| priority | int32_t | [Font](../../../aspose.words/font/) prioridad de origen. Consulte la descripción de la propiedad [Priority](../../fontsourcebase/get_priority/) para obtener más información. |

## Ejemplos



Muestra cómo usar una matriz de bytes con datos de un archivo de fuente como una fuente.
```cpp
System::ArrayPtr<uint8_t> fontBytes = System::IO::File::ReadAllBytes(get_MyDir() + u"Alte DIN 1451 Mittelschrift.ttf");
auto memoryFontSource = System::MakeObject<Aspose::Words::Fonts::MemoryFontSource>(fontBytes, 0);

auto doc = System::MakeObject<Aspose::Words::Document>();
doc->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());
doc->get_FontSettings()->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({memoryFontSource}));

ASSERT_EQ(Aspose::Words::Fonts::FontSourceType::MemoryFont, memoryFontSource->get_Type());
ASSERT_EQ(0, memoryFontSource->get_Priority());
```

## Ver también

* Class [MemoryFontSource](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
## MemoryFontSource::MemoryFontSource(const System::ArrayPtr\<uint8_t\>\&, int32_t, const System::String\&) constructor


Ctor.

```cpp
Aspose::Words::Fonts::MemoryFontSource::MemoryFontSource(const System::ArrayPtr<uint8_t> &fontData, int32_t priority, const System::String &cacheKey)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| fontData | const System::ArrayPtr\<uint8_t\>\& | Datos de fuente binarios. |
| priority | int32_t | [Font](../../../aspose.words/font/) prioridad de origen. Consulte la descripción de la propiedad [Priority](../../fontsourcebase/get_priority/) para obtener más información. |
| cacheKey | const System::String\& | La clave de esta fuente en la caché. Consulte la descripción de la propiedad [CacheKey](../get_cachekey/) para obtener más información. |

## Ver también

* Class [MemoryFontSource](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
