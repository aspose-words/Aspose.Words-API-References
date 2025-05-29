---
title: FontFallbackSettings.Save
linktitle: Save
articleTitle: Save
second_title: Aspose.Words для .NET
description: Легко сохраняйте FontFallbackSettings с помощью нашего интуитивно понятного метода Save. Сохраняйте свои пользовательские настройки резервного копирования для бесперебойного управления шрифтами.
type: docs
weight: 50
url: /ru/net/aspose.words.fonts/fontfallbacksettings/save/
---
## Save(*Stream*) {#save}

Сохраняет текущие резервные настройки в потоке.

```csharp
public void Save(Stream outputStream)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| outputStream | Stream | Выходной поток. |

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

---

## Save(*string*) {#save_1}

Сохраняет текущие резервные настройки в файл.

```csharp
public void Save(string fileName)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| fileName | String | Имя выходного файла. |

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
