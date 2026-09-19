---
title: "enum Aspose::Words::Fonts::FontSourceType"
linktitle: "FontSourceType"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fonts::FontSourceType enum. Specifica il tipo di origine del font in C++."
type: docs
weight: 23000
url: /it/cpp/aspose.words.fonts/fontsourcetype/
---
## FontSourceType enum


Specifica il tipo di sorgente del carattere.

```cpp
enum class FontSourceType
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| FontFile | 0 | Un oggetto [FileFontSource](../filefontsource/) che rappresenta un singolo file di font. |
| FontsFolder | 1 | Un oggetto [FolderFontSource](../folderfontsource/) che rappresenta una cartella con file di font. |
| MemoryFont | 2 | Un oggetto [MemoryFontSource](../memoryfontsource/) che rappresenta un singolo font in memoria. |
| SystemFonts | 3 | Un oggetto [SystemFontSource](../systemfontsource/) che rappresenta tutti i font installati nel sistema. |
| FontStream | 4 | Un oggetto [StreamFontSource](../streamfontsource/) che rappresenta un flusso con dati di font. |


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

* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
