---
title: Priority
second_title: Справочник по API Aspose.Words для .NET
description: Возвращает приоритет источника шрифта.
type: docs
weight: 10
url: /ru/net/aspose.words.fonts/fontsourcebase/priority/
---
## FontSourceBase.Priority property

Возвращает приоритет источника шрифта.

```csharp
public int Priority { get; }
```

### Примечания

Это значение используется при наличии шрифтов с одинаковым именем семейства и стилем в разных источниках шрифтов. В этом случае Aspose.Words выбирает шрифт из источника с более высоким значением приоритета.

Значение по умолчанию — 0.

### Примеры

Показывает, как использовать файл шрифта в локальной файловой системе в качестве источника шрифта.

```csharp
FileFontSource fileFontSource = new FileFontSource(MyDir + "Alte DIN 1451 Mittelschrift.ttf", 0);

Document doc = new Document();
doc.FontSettings = new FontSettings();
doc.FontSettings.SetFontsSources(new FontSourceBase[] {fileFontSource});

Assert.AreEqual(MyDir + "Alte DIN 1451 Mittelschrift.ttf", fileFontSource.FilePath);
Assert.AreEqual(FontSourceType.FontFile, fileFontSource.Type);
Assert.AreEqual(0, fileFontSource.Priority);
```

### Смотрите также

* class [FontSourceBase](../../fontsourcebase)
* пространство имен [Aspose.Words.Fonts](../../fontsourcebase)
* сборка [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
