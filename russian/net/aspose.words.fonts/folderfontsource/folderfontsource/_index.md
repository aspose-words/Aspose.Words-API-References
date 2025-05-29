---
title: FolderFontSource
linktitle: FolderFontSource
articleTitle: FolderFontSource
second_title: Aspose.Words для .NET
description: Откройте для себя конструктор FolderFontSource для бесшовного управления шрифтами. Улучшите свои веб-проекты с помощью эффективного поиска шрифтов уже сегодня!
type: docs
weight: 10
url: /ru/net/aspose.words.fonts/folderfontsource/folderfontsource/
---
## FolderFontSource(*string, bool*) {#constructor}

Ctor.

```csharp
public FolderFontSource(string folderPath, bool scanSubfolders)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| folderPath | String | Путь к папке. |
| scanSubfolders | Boolean | Определяет, следует ли сканировать подпапки. |

## Примеры

Показывает, как использовать локальную системную папку, содержащую шрифты, в качестве источника шрифтов.

```csharp
// Создаем источник шрифтов из папки, содержащей файлы шрифтов.
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, false, 1);

Document doc = new Document();
doc.FontSettings = new FontSettings();
doc.FontSettings.SetFontsSources(new FontSourceBase[] {folderFontSource});

Assert.AreEqual(FontsDir, folderFontSource.FolderPath);
Assert.AreEqual(false, folderFontSource.ScanSubfolders);
Assert.AreEqual(FontSourceType.FontsFolder, folderFontSource.Type);
Assert.AreEqual(1, folderFontSource.Priority);
```

### Смотрите также

* class [FolderFontSource](../)
* пространство имен [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* сборка [Aspose.Words](../../../)

---

## FolderFontSource(*string, bool, int*) {#constructor_1}

Ctor.

```csharp
public FolderFontSource(string folderPath, bool scanSubfolders, int priority)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| folderPath | String | Путь к папке. |
| scanSubfolders | Boolean | Определяет, следует ли сканировать подпапки. |
| priority | Int32 | Приоритет источника шрифта. См.[`Priority`](../../fontsourcebase/priority/) описание недвижимости для получения более подробной информации. |

## Примеры

Показывает, как использовать локальную системную папку, содержащую шрифты, в качестве источника шрифтов.

```csharp
// Создаем источник шрифтов из папки, содержащей файлы шрифтов.
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, false, 1);

Document doc = new Document();
doc.FontSettings = new FontSettings();
doc.FontSettings.SetFontsSources(new FontSourceBase[] {folderFontSource});

Assert.AreEqual(FontsDir, folderFontSource.FolderPath);
Assert.AreEqual(false, folderFontSource.ScanSubfolders);
Assert.AreEqual(FontSourceType.FontsFolder, folderFontSource.Type);
Assert.AreEqual(1, folderFontSource.Priority);
```

### Смотрите также

* class [FolderFontSource](../)
* пространство имен [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* сборка [Aspose.Words](../../../)
