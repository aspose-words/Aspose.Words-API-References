---
title: FontFallbackSettings.BuildAutomatic
linktitle: BuildAutomatic
articleTitle: BuildAutomatic
second_title: Aspose.Words для .NET
description: Откройте для себя метод FontFallbackSettings BuildAutomatic, который легко сканирует шрифты, чтобы создать оптимальные резервные настройки для улучшенной типографики.
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

Этот метод может привести к неоптимальным резервным настройкам. Шрифты проверяются[ Диапазон символов Unicode](https://docs.microsoft.com/en-us/typography/opentype/spec/os2#ur) поля, а не фактическое наличие глифов. Также диапазоны Unicode проверяются индивидуально и несколько диапазонов, связанных с одним языком/сценарием, могут использовать разные резервные шрифты.

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

* class [FontFallbackSettings](../)
* пространство имен [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* сборка [Aspose.Words](../../../)
