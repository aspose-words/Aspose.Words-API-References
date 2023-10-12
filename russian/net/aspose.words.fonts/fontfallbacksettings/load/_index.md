---
title: FontFallbackSettings.Load
second_title: Справочник по API Aspose.Words для .NET
description: FontFallbackSettings метод. Загружает настройки резервного шрифта из XMLфайла.
type: docs
weight: 20
url: /ru/net/aspose.words.fonts/fontfallbacksettings/load/
---
## Load(string) {#load_1}

Загружает настройки резервного шрифта из XML-файла.

```csharp
public void Load(string fileName)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| fileName | String | Имя входного файла. |

### Примеры

Показывает, как загрузить и сохранить настройки резервного шрифта в XML-документе в локальной файловой системе или из него.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Загрузите XML-документ, который определяет набор резервных настроек шрифта.
FontSettings fontSettings = new FontSettings();
fontSettings.FallbackSettings.Load(MyDir + "Font fallback rules.xml");

doc.FontSettings = fontSettings;
doc.Save(ArtifactsDir + "FontSettings.LoadFontFallbackSettingsFromFile.pdf");

// Сохраняем текущие настройки резервного шрифта нашего документа как XML-документ.
doc.FontSettings.FallbackSettings.Save(ArtifactsDir + "FallbackSettings.xml");
```

### Смотрите также

* class [FontFallbackSettings](../)
* пространство имен [Aspose.Words.Fonts](../../fontfallbacksettings/)
* сборка [Aspose.Words](../../../)

---

## Load(Stream) {#load}

Загружает резервные настройки из потока XML.

```csharp
public void Load(Stream stream)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| stream | Stream | Входной поток. |

### Примеры

Показывает, как загрузить и сохранить настройки резервного шрифта в поток или из него.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Загрузите XML-документ, который определяет набор резервных настроек шрифта.
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

* class [FontFallbackSettings](../)
* пространство имен [Aspose.Words.Fonts](../../fontfallbacksettings/)
* сборка [Aspose.Words](../../../)


