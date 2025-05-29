---
title: FontFallbackSettings.Load
linktitle: Load
articleTitle: Load
second_title: Aspose.Words для .NET
description: Простая загрузка и управление настройками резервных шрифтов из XML-файлов с помощью метода FontFallbackSettings Load для бесшовной интеграции типографики.
type: docs
weight: 20
url: /ru/net/aspose.words.fonts/fontfallbacksettings/load/
---
## Load(*string*) {#load_1}

Загружает настройки резервного шрифта из XML-файла.

```csharp
public void Load(string fileName)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| fileName | String | Имя входного файла. |

## Примеры

Показывает, как загружать и сохранять настройки резервного шрифта в/из XML-документа в локальной файловой системе.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Загрузить XML-документ, определяющий набор настроек резервного шрифта.
FontSettings fontSettings = new FontSettings();
fontSettings.FallbackSettings.Load(MyDir + "Font fallback rules.xml");

doc.FontSettings = fontSettings;
doc.Save(ArtifactsDir + "FontSettings.LoadFontFallbackSettingsFromFile.pdf");

// Сохраняем текущие настройки резервного шрифта нашего документа как XML-документ.
doc.FontSettings.FallbackSettings.Save(ArtifactsDir + "FallbackSettings.xml");
```

### Смотрите также

* class [FontFallbackSettings](../)
* пространство имен [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* сборка [Aspose.Words](../../../)

---

## Load(*Stream*) {#load}

Загружает резервные настройки из потока XML.

```csharp
public void Load(Stream stream)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| stream | Stream | Входной поток. |

## Примеры

Показывает, как загружать и сохранять настройки резервного шрифта в/из потока.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Загрузить XML-документ, определяющий набор настроек резервного шрифта.
using (FileStream fontFallbackStream = new FileStream(MyDir + "Font fallback rules.xml", FileMode.Open))
{
    FontSettings fontSettings = new FontSettings();
    fontSettings.FallbackSettings.Load(fontFallbackStream);

    doc.FontSettings = fontSettings;
}

doc.Save(ArtifactsDir + "FontSettings.LoadFontFallbackSettingsFromStream.pdf");

// Используем поток для сохранения текущих настроек резервного шрифта нашего документа в виде XML-документа.
using (FileStream fontFallbackStream =
    new FileStream(ArtifactsDir + "FallbackSettings.xml", FileMode.Create))
{
    doc.FontSettings.FallbackSettings.Save(fontFallbackStream);
}
```

### Смотрите также

* class [FontFallbackSettings](../)
* пространство имен [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* сборка [Aspose.Words](../../../)
