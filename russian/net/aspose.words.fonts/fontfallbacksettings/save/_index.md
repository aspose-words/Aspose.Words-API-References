---
title: FontFallbackSettings.Save
linktitle: Save
articleTitle: Save
second_title: Aspose.Words для .NET
description: FontFallbackSettings Save метод. Сохраняет текущие резервные настройки в потоковом режиме на С#.
type: docs
weight: 50
url: /ru/net/aspose.words.fonts/fontfallbacksettings/save/
---
## Save(*Stream*) {#save}

Сохраняет текущие резервные настройки в потоковом режиме.

```csharp
public void Save(Stream outputStream)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| outputStream | Stream | Выходной поток. |

## Примеры

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
* пространство имен [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* сборка [Aspose.Words](../../../)
