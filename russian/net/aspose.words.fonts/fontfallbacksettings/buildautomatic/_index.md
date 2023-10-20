---
title: FontFallbackSettings.BuildAutomatic
linktitle: BuildAutomatic
articleTitle: BuildAutomatic
second_title: Aspose.Words для .NET
description: FontFallbackSettings BuildAutomatic метод. Автоматически создает резервные настройки путем сканирования доступных шрифтов на С#.
type: docs
weight: 10
url: /ru/net/aspose.words.fonts/fontfallbacksettings/buildautomatic/
---
## FontFallbackSettings.BuildAutomatic method

Автоматически создает резервные настройки путем сканирования доступных шрифтов.

```csharp
public void BuildAutomatic()
```

## Примечания

Этот метод может привести к неоптимальным резервным настройкам. Шрифты проверяются[ Диапазон символов Юникода](https://docs.microsoft.com/en-us/typography/opentype/spec/os2#ur) поля, а не фактическое наличие глифов. Также диапазоны Юникода проверяются индивидуально , и несколько диапазонов, связанных с одним языком/скриптом, могут использовать разные резервные шрифты.

## Примеры

Показывает, как распределять резервные шрифты по диапазонам кодов символов Юникода.

```csharp
Document doc = new Document();

FontSettings fontSettings = new FontSettings();
doc.FontSettings = fontSettings;
FontFallbackSettings fontFallbackSettings = fontSettings.FallbackSettings;

// Настройте наши настройки шрифтов так, чтобы исходные шрифты были только из папки «MyFonts».
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, false);
fontSettings.SetFontsSources(new FontSourceBase[] {folderFontSource});

// Вызов метода "BuildAutomatic" сгенерирует резервную схему, которая
// распределяет доступные шрифты по как можно большему количеству кодов символов Юникода.
// В нашем случае у него есть доступ только к небольшому количеству шрифтов в папке «MyFonts».
fontFallbackSettings.BuildAutomatic();
fontFallbackSettings.Save(ArtifactsDir + "FontSettings.FallbackSettingsCustom.BuildAutomatic.xml");

// Мы также можем загрузить собственную схему замены из такого файла.
// Эта схема применяет шрифт «AllegroOpen» к блокам Юникода «0000-00ff», шрифт «AllegroOpen» к блокам «0100-024f»,
// и шрифт «M+ 2m» во всех остальных диапазонах, которые не охватываются другими шрифтами в схеме.
fontFallbackSettings.Load(MyDir + "Custom font fallback settings.xml");

// Создаем конструктор документов и устанавливаем для него шрифт, которого нет ни в одном из наших источников.
// Наши настройки шрифта будут вызывать резервную схему для символов, которые мы печатаем с использованием недоступного шрифта.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Font.Name = "Missing Font";

// Используйте конструктор для печати каждого символа Юникода от 0x0021 до 0x052F,
// с описательными линиями, разделяющими блоки Юникода, которые мы определили в нашей резервной схеме пользовательского шрифта.
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

* class [FontFallbackSettings](../)
* пространство имен [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* сборка [Aspose.Words](../../../)
