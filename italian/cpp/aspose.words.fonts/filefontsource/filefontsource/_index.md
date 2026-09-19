---
title: "Aspose::Words::Fonts::FileFontSource::FileFontSource costruttore"
linktitle: "FileFontSource"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fonts::FileFontSource::FileFontSource costruttore. Ctor in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words.fonts/filefontsource/filefontsource/
---
## FileFontSource::FileFontSource(const System::String\&) constructor


Costruttore.

```cpp
Aspose::Words::Fonts::FileFontSource::FileFontSource(const System::String &filePath)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| filePath | const System::String\& | Percorso al file del font. |

## Esempi



Mostra come utilizzare un file di font nel file system locale come origine del font.
```cpp
auto fileFontSource = System::MakeObject<Aspose::Words::Fonts::FileFontSource>(get_MyDir() + u"Alte DIN 1451 Mittelschrift.ttf", 0);

auto doc = System::MakeObject<Aspose::Words::Document>();
doc->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());
doc->get_FontSettings()->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({fileFontSource}));

ASSERT_EQ(get_MyDir() + u"Alte DIN 1451 Mittelschrift.ttf", fileFontSource->get_FilePath());
ASSERT_EQ(Aspose::Words::Fonts::FontSourceType::FontFile, fileFontSource->get_Type());
ASSERT_EQ(0, fileFontSource->get_Priority());
```

## Vedi anche

* Class [FileFontSource](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
## FileFontSource::FileFontSource(const System::String\&, int32_t) constructor


Costruttore.

```cpp
Aspose::Words::Fonts::FileFontSource::FileFontSource(const System::String &filePath, int32_t priority)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| filePath | const System::String\& | Percorso al file del font. |
| priority | int32_t | [Font](../../../aspose.words/font/) priorità della sorgente. Vedi la descrizione della proprietà [Priority](../../fontsourcebase/get_priority/) per ulteriori informazioni. |

## Esempi



Mostra come utilizzare un file di font nel file system locale come origine del font.
```cpp
auto fileFontSource = System::MakeObject<Aspose::Words::Fonts::FileFontSource>(get_MyDir() + u"Alte DIN 1451 Mittelschrift.ttf", 0);

auto doc = System::MakeObject<Aspose::Words::Document>();
doc->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());
doc->get_FontSettings()->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({fileFontSource}));

ASSERT_EQ(get_MyDir() + u"Alte DIN 1451 Mittelschrift.ttf", fileFontSource->get_FilePath());
ASSERT_EQ(Aspose::Words::Fonts::FontSourceType::FontFile, fileFontSource->get_Type());
ASSERT_EQ(0, fileFontSource->get_Priority());
```

## Vedi anche

* Class [FileFontSource](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
## FileFontSource::FileFontSource(const System::String\&, int32_t, const System::String\&) constructor


Costruttore.

```cpp
Aspose::Words::Fonts::FileFontSource::FileFontSource(const System::String &filePath, int32_t priority, const System::String &cacheKey)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| filePath | const System::String\& | Percorso al file del font. |
| priority | int32_t | [Font](../../../aspose.words/font/) priorità della sorgente. Vedi la descrizione della proprietà [Priority](../../fontsourcebase/get_priority/) per ulteriori informazioni. |
| cacheKey | const System::String\& | La chiave di questa origine nella cache. Vedi la descrizione della proprietà [CacheKey](../get_cachekey/) per maggiori informazioni. |

## Vedi anche

* Class [FileFontSource](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
