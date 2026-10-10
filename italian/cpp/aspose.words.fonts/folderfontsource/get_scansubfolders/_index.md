---
title: "Metodo Aspose::Words::Fonts::FolderFontSource::get_ScanSubfolders"
linktitle: "get_ScanSubfolders"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Fonts::FolderFontSource::get_ScanSubfolders. Determina se eseguire o meno la scansione delle sottocartelle in C++."
type: docs
weight: 4000
url: /it/cpp/aspose.words.fonts/folderfontsource/get_scansubfolders/
---
## FolderFontSource::get_ScanSubfolders method


Determina se eseguire o meno la scansione delle sottocartelle.

```cpp
bool Aspose::Words::Fonts::FolderFontSource::get_ScanSubfolders() const
```


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
