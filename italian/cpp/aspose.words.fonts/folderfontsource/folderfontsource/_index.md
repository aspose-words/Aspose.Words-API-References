---
title: "Aspose::Words::Fonts::FolderFontSource::FolderFontSource costruttore"
linktitle: "FolderFontSource"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fonts::FolderFontSource::FolderFontSource costruttore. Ctor in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words.fonts/folderfontsource/folderfontsource/
---
## FolderFontSource::FolderFontSource(const System::String\&, bool) constructor


Costruttore.

```cpp
Aspose::Words::Fonts::FolderFontSource::FolderFontSource(const System::String &folderPath, bool scanSubfolders)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| folderPath | const System::String\& | Percorso della cartella. |
| scanSubfolders | bool | Determina se eseguire o meno la scansione delle sottocartelle. |

## Esempi



Mostra come utilizzare una cartella di sistema locale che contiene font come sorgente di font.
```cpp
// Crea una sorgente di font da una cartella che contiene file di font.
auto folderFontSource = System::MakeObject<Aspose::Words::Fonts::FolderFontSource>(get_FontsDir(), false, 1);

auto doc = System::MakeObject<Aspose::Words::Document>();
doc->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());
doc->get_FontSettings()->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({folderFontSource}));

ASSERT_EQ(get_FontsDir(), folderFontSource->get_FolderPath());
ASPOSE_ASSERT_EQ(false, folderFontSource->get_ScanSubfolders());
ASSERT_EQ(Aspose::Words::Fonts::FontSourceType::FontsFolder, folderFontSource->get_Type());
ASSERT_EQ(1, folderFontSource->get_Priority());
```

## Vedi anche

* Class [FolderFontSource](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
## FolderFontSource::FolderFontSource(const System::String\&, bool, int32_t) constructor


Costruttore.

```cpp
Aspose::Words::Fonts::FolderFontSource::FolderFontSource(const System::String &folderPath, bool scanSubfolders, int32_t priority)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| folderPath | const System::String\& | Percorso della cartella. |
| scanSubfolders | bool | Determina se eseguire o meno la scansione delle sottocartelle. |
| priority | int32_t | [Font](../../../aspose.words/font/) priorità della sorgente. Vedi la descrizione della proprietà [Priority](../../fontsourcebase/get_priority/) per ulteriori informazioni. |

## Esempi



Mostra come utilizzare una cartella di sistema locale che contiene font come sorgente di font.
```cpp
// Crea una sorgente di font da una cartella che contiene file di font.
auto folderFontSource = System::MakeObject<Aspose::Words::Fonts::FolderFontSource>(get_FontsDir(), false, 1);

auto doc = System::MakeObject<Aspose::Words::Document>();
doc->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());
doc->get_FontSettings()->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({folderFontSource}));

ASSERT_EQ(get_FontsDir(), folderFontSource->get_FolderPath());
ASPOSE_ASSERT_EQ(false, folderFontSource->get_ScanSubfolders());
ASSERT_EQ(Aspose::Words::Fonts::FontSourceType::FontsFolder, folderFontSource->get_Type());
ASSERT_EQ(1, folderFontSource->get_Priority());
```

## Vedi anche

* Class [FolderFontSource](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
