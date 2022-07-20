---
title: Save
second_title: Справочник по API Aspose.Words для .NET
description: Сохраняет текущие резервные настройки в потоке.
type: docs
weight: 50
url: /ru/net/aspose.words.fonts/fontfallbacksettings/save/
---
## Save(Stream) {#save}

Сохраняет текущие резервные настройки в потоке.

```csharp
public void Save(Stream outputStream)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| outputStream | Stream | Выходной поток. |

### Примеры

Показывает, как загружать и сохранять резервные настройки шрифта в/из потока.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Загружаем XML-документ, определяющий набор резервных настроек шрифта.
using (FileStream fontFallbackStream = new FileStream(MyDir + "Font fallback rules.xml", FileMode.Open))
{
    FontSettings fontSettings = new FontSettings();
    fontSettings.FallbackSettings.Load(fontFallbackStream);

    doc.FontSettings = fontSettings;
}

doc.Save(ArtifactsDir + "FontSettings.LoadFontFallbackSettingsFromStream.pdf");

// Используйте поток, чтобы сохранить текущие настройки резервного шрифта нашего документа в виде XML-документа.
using (FileStream fontFallbackStream =
    new FileStream(ArtifactsDir + "FallbackSettings.xml", FileMode.Create))
{
    doc.FontSettings.FallbackSettings.Save(fontFallbackStream);
}
```

### Смотрите также

* class [FontFallbackSettings](../../fontfallbacksettings)
* пространство имен [Aspose.Words.Fonts](../../fontfallbacksettings)
* сборка [Aspose.Words](../../../)

---

## Save(string) {#save_1}

Сохраняет текущие резервные настройки в файл.

```csharp
public void Save(string fileName)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| fileName | String | Имя выходного файла. |

### Примеры

Показывает, как загружать и сохранять резервные настройки шрифта в/из XML-документа в локальной файловой системе.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Загружаем XML-документ, определяющий набор резервных настроек шрифта.
FontSettings fontSettings = new FontSettings();
fontSettings.FallbackSettings.Load(MyDir + "Font fallback rules.xml");

doc.FontSettings = fontSettings;
doc.Save(ArtifactsDir + "FontSettings.LoadFontFallbackSettingsFromFile.pdf");

// Сохраняем текущие настройки резервного шрифта нашего документа в виде XML-документа.
doc.FontSettings.FallbackSettings.Save(ArtifactsDir + "FallbackSettings.xml");
```

### Смотрите также

* class [FontFallbackSettings](../../fontfallbacksettings)
* пространство имен [Aspose.Words.Fonts](../../fontfallbacksettings)
* сборка [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->