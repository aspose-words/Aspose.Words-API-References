---
title: FontFallbackSettings Class
linktitle: FontFallbackSettings
articleTitle: FontFallbackSettings
second_title: Aspose.Words для .NET
description: Откройте для себя Aspose.Words.Fonts.FontFallbackSettings для настраиваемых параметров резервного шрифта, обеспечивающих плавную визуализацию документов и улучшенное отображение текста.
type: docs
weight: 3330
url: /ru/net/aspose.words.fonts/fontfallbacksettings/
---
## FontFallbackSettings class

Задает настройки механизма резервного копирования шрифтов.

Чтобы узнать больше, посетите[Работа со шрифтами](https://docs.aspose.com/words/net/working-with-fonts/) документальная статья.

```csharp
public class FontFallbackSettings
```

## Методы

| Имя | Описание |
| --- | --- |
| [BuildAutomatic](../../aspose.words.fonts/fontfallbacksettings/buildautomatic/)() | Автоматически создает резервные настройки путем сканирования доступных шрифтов. |
| [Load](../../aspose.words.fonts/fontfallbacksettings/load/#load)(*Stream*) | Загружает резервные настройки из потока XML. |
| [Load](../../aspose.words.fonts/fontfallbacksettings/load/#load_1)(*string*) | Загружает настройки резервного шрифта из XML-файла. |
| [LoadMsOfficeFallbackSettings](../../aspose.words.fonts/fontfallbacksettings/loadmsofficefallbacksettings/)() | Загружает предопределенные резервные настройки, которые имитируют резервные настройки Microsoft Word и используют шрифты Microsoft Office. |
| [LoadNotoFallbackSettings](../../aspose.words.fonts/fontfallbacksettings/loadnotofallbacksettings/)() | Загружает предопределенные резервные настройки, которые используют шрифты Google Noto. |
| [Save](../../aspose.words.fonts/fontfallbacksettings/save/#save)(*Stream*) | Сохраняет текущие резервные настройки в потоке. |
| [Save](../../aspose.words.fonts/fontfallbacksettings/save/#save_1)(*string*) | Сохраняет текущие резервные настройки в файл. |

## Примечания

По умолчанию резервные настройки инициализируются с предопределенными настройками, которые имитируют резервные настройки Microsoft Word.

## Примеры

Показывает, как распределить резервные шрифты по диапазонам кодов символов Unicode.

```csharp
Document doc = new Document();

FontSettings fontSettings = new FontSettings();
doc.FontSettings = fontSettings;
FontFallbackSettings fontFallbackSettings = fontSettings.FallbackSettings;

// Настраиваем параметры шрифтов так, чтобы они брались только из папки «MyFonts».
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, false);
fontSettings.SetFontsSources(new FontSourceBase[] {folderFontSource});

// Вызов метода "BuildAutomatic" сгенерирует резервную схему, которая
// распределяет доступные шрифты по максимально возможному количеству кодов символов Unicode.
// В нашем случае он имеет доступ только к нескольким шрифтам внутри папки «MyFonts».
fontFallbackSettings.BuildAutomatic();
fontFallbackSettings.Save(ArtifactsDir + "FontSettings.FallbackSettingsCustom.BuildAutomatic.xml");

// Мы также можем загрузить пользовательскую схему замены из файла, подобного этому.
// Эта схема применяет шрифт "AllegroOpen" к блокам Unicode "0000-00ff", шрифт "AllegroOpen" к блокам "0100-024f",
// и шрифт "M+ 2m" во всех других диапазонах, которые не покрываются другими шрифтами в схеме.
fontFallbackSettings.Load(MyDir + "Custom font fallback settings.xml");

// Создаем конструктор документов и устанавливаем для него шрифт, которого нет ни в одном из наших источников.
// Наши настройки шрифта будут вызывать резервную схему для символов, которые мы печатаем с использованием недоступного шрифта.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Font.Name = "Missing Font";

// Используйте конструктор для печати каждого символа Unicode от 0x0021 до 0x052F,
// с описательными линиями, разделяющими блоки Unicode, которые мы определили в нашей пользовательской схеме резервного шрифта.
for (int i = 0x0021; i < 0x0530; i++)
{
    switch (i)
    {
        case 0x0021:
            builder.Writeln(
                "\n\n0x0021 - 0x00FF: \nBasic Latin/Latin-1 Supplement Unicode blocks in \"AllegroOpen\" font:");
            break;
        case 0x0100:
            builder.Writeln(
                "\n\n0x0100 - 0x024F: \nLatin Extended A/B blocks, mostly in \"AllegroOpen\" font:");
            break;
        case 0x0250:
            builder.Writeln("\n\n0x0250 - 0x052F: \nIPA/Greek/Cyrillic blocks in \"M+ 2m\" font:");
            break;
    }

    builder.Write($"{Convert.ToChar(i)}");
}

doc.Save(ArtifactsDir + "FontSettings.FallbackSettingsCustom.pdf");
```

### Смотрите также

* пространство имен [Aspose.Words.Fonts](../../aspose.words.fonts/)
* сборка [Aspose.Words](../../)
