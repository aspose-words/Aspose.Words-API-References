---
title: "Aspose::Words::Fonts::FolderFontSource::FolderFontSource constructor"
linktitle: "FolderFontSource"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fonts::FolderFontSource::FolderFontSource konstruktor. Konstruktor i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words.fonts/folderfontsource/folderfontsource/
---
## FolderFontSource::FolderFontSource(const System::String\&, bool) constructor


Konstruktör.

```cpp
Aspose::Words::Fonts::FolderFontSource::FolderFontSource(const System::String &folderPath, bool scanSubfolders)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| folderPath | const System::String\& | Sökväg till mapp. |
| scanSubfolders | bool | Bestämmer om underkataloger ska skannas eller inte. |

## Exempel



Visar hur man använder en lokal systemmapp som innehåller teckensnitt som en teckensnittskälla.
```cpp
// Skapa en teckensnittskälla från en mapp som innehåller teckensnittsfiler.
auto folderFontSource = System::MakeObject<Aspose::Words::Fonts::FolderFontSource>(get_FontsDir(), false, 1);

auto doc = System::MakeObject<Aspose::Words::Document>();
doc->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());
doc->get_FontSettings()->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({folderFontSource}));

ASSERT_EQ(get_FontsDir(), folderFontSource->get_FolderPath());
ASPOSE_ASSERT_EQ(false, folderFontSource->get_ScanSubfolders());
ASSERT_EQ(Aspose::Words::Fonts::FontSourceType::FontsFolder, folderFontSource->get_Type());
ASSERT_EQ(1, folderFontSource->get_Priority());
```

## Se även

* Class [FolderFontSource](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
## FolderFontSource::FolderFontSource(const System::String\&, bool, int32_t) constructor


Konstruktör.

```cpp
Aspose::Words::Fonts::FolderFontSource::FolderFontSource(const System::String &folderPath, bool scanSubfolders, int32_t priority)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| folderPath | const System::String\& | Sökväg till mapp. |
| scanSubfolders | bool | Bestämmer om underkataloger ska skannas eller inte. |
| priority | int32_t | [Font](../../../aspose.words/font/) källprioritet. Se beskrivningen av egenskapen [Priority](../../fontsourcebase/get_priority/) för mer information. |

## Exempel



Visar hur man använder en lokal systemmapp som innehåller teckensnitt som en teckensnittskälla.
```cpp
// Skapa en teckensnittskälla från en mapp som innehåller teckensnittsfiler.
auto folderFontSource = System::MakeObject<Aspose::Words::Fonts::FolderFontSource>(get_FontsDir(), false, 1);

auto doc = System::MakeObject<Aspose::Words::Document>();
doc->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());
doc->get_FontSettings()->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({folderFontSource}));

ASSERT_EQ(get_FontsDir(), folderFontSource->get_FolderPath());
ASPOSE_ASSERT_EQ(false, folderFontSource->get_ScanSubfolders());
ASSERT_EQ(Aspose::Words::Fonts::FontSourceType::FontsFolder, folderFontSource->get_Type());
ASSERT_EQ(1, folderFontSource->get_Priority());
```

## Se även

* Class [FolderFontSource](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
