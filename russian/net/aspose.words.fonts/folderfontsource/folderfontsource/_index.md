---
title: FolderFontSource.FolderFontSource
second_title: Справочник по API Aspose.Words для .NET
description: FolderFontSource строитель. Cтор.
type: docs
weight: 10
url: /ru/net/aspose.words.fonts/folderfontsource/folderfontsource/
---
## FolderFontSource(string, bool) {#constructor}

Cтор.

```csharp
public FolderFontSource(string folderPath, bool scanSubfolders)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| folderPath | String | Путь к папке. |
| scanSubfolders | Boolean | Определяет, сканировать ли подпапки. |

### Примеры

Показывает, как использовать локальную системную папку, содержащую шрифты, в качестве источника шрифтов.

```csharp
// Создать источник шрифта из папки, содержащей файлы шрифтов.
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
* пространство имен [Aspose.Words.Fonts](../../folderfontsource/)
* сборка [Aspose.Words](../../../)

---

## FolderFontSource(string, bool, int) {#constructor_1}

Cтор.

```csharp
public FolderFontSource(string folderPath, bool scanSubfolders, int priority)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| folderPath | String | Путь к папке. |
| scanSubfolders | Boolean | Определяет, сканировать ли подпапки. |
| priority | Int32 | Приоритет источника шрифта. См.[`Priority`](../../fontsourcebase/priority/) описание недвижимости для получения дополнительной информации. |

### Примеры

Показывает, как использовать локальную системную папку, содержащую шрифты, в качестве источника шрифтов.

```csharp
// Создать источник шрифта из папки, содержащей файлы шрифтов.
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
* пространство имен [Aspose.Words.Fonts](../../folderfontsource/)
* сборка [Aspose.Words](../../../)


