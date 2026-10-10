---
title: "Aspose::Words::Fonts::FolderFontSource::FolderFontSource Konstruktor"
linktitle: "FolderFontSource"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fonts::FolderFontSource::FolderFontSource Konstruktor. Konstruktor in C++."
type: docs
weight: 2000
url: /de/cpp/aspose.words.fonts/folderfontsource/folderfontsource/
---
## FolderFontSource::FolderFontSource(const System::String\&, bool) constructor


Konstruktor.

```cpp
Aspose::Words::Fonts::FolderFontSource::FolderFontSource(const System::String &folderPath, bool scanSubfolders)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| folderPath | const System::String\& | Pfad zum Ordner. |
| scanSubfolders | bool | Bestimmt, ob Unterordner gescannt werden sollen oder nicht. |

## Beispiele



Zeigt, wie ein lokaler Systemordner, der Schriften enthält, als Schriftquelle verwendet wird.
```cpp
// Erstellen Sie eine Schriftquelle aus einem Ordner, der Schriftdateien enthält.
auto folderFontSource = System::MakeObject<Aspose::Words::Fonts::FolderFontSource>(get_FontsDir(), false, 1);

auto doc = System::MakeObject<Aspose::Words::Document>();
doc->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());
doc->get_FontSettings()->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({folderFontSource}));

ASSERT_EQ(get_FontsDir(), folderFontSource->get_FolderPath());
ASPOSE_ASSERT_EQ(false, folderFontSource->get_ScanSubfolders());
ASSERT_EQ(Aspose::Words::Fonts::FontSourceType::FontsFolder, folderFontSource->get_Type());
ASSERT_EQ(1, folderFontSource->get_Priority());
```

## Siehe auch

* Class [FolderFontSource](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
## FolderFontSource::FolderFontSource(const System::String\&, bool, int32_t) constructor


Konstruktor.

```cpp
Aspose::Words::Fonts::FolderFontSource::FolderFontSource(const System::String &folderPath, bool scanSubfolders, int32_t priority)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| folderPath | const System::String\& | Pfad zum Ordner. |
| scanSubfolders | bool | Bestimmt, ob Unterordner gescannt werden sollen oder nicht. |
| priority | int32_t | [Font](../../../aspose.words/font/) Quellpriorität. Siehe die [Priority](../../fontsourcebase/get_priority/) Eigenschaftsbeschreibung für weitere Informationen. |

## Beispiele



Zeigt, wie ein lokaler Systemordner, der Schriften enthält, als Schriftquelle verwendet wird.
```cpp
// Erstellen Sie eine Schriftquelle aus einem Ordner, der Schriftdateien enthält.
auto folderFontSource = System::MakeObject<Aspose::Words::Fonts::FolderFontSource>(get_FontsDir(), false, 1);

auto doc = System::MakeObject<Aspose::Words::Document>();
doc->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());
doc->get_FontSettings()->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({folderFontSource}));

ASSERT_EQ(get_FontsDir(), folderFontSource->get_FolderPath());
ASPOSE_ASSERT_EQ(false, folderFontSource->get_ScanSubfolders());
ASSERT_EQ(Aspose::Words::Fonts::FontSourceType::FontsFolder, folderFontSource->get_Type());
ASSERT_EQ(1, folderFontSource->get_Priority());
```

## Siehe auch

* Class [FolderFontSource](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
