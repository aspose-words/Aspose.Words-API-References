---
title: FontInfo.Name
linktitle: Name
articleTitle: Name
second_title: Aspose.Words для .NET
description: Откройте для себя свойство FontInfo Name, чтобы легко получать доступ к названиям шрифтов и использовать их для улучшения типографики в ваших проектах.
type: docs
weight: 60
url: /ru/net/aspose.words.fonts/fontinfo/name/
---
## FontInfo.Name property

Получает имя шрифта.

```csharp
public string Name { get; }
```

## Примечания

Не может быть`нулевой`. Может быть пустой строкой.

## Примеры

Показывает, как распечатать подробную информацию о шрифтах, присутствующих в документе.

```csharp
Document doc = new Document(MyDir + "Embedded font.docx");

FontInfoCollection allFonts = doc.FontInfos;
// Распечатать все используемые и неиспользуемые шрифты в документе.
for (int i = 0; i < allFonts.Count; i++)
{
    Console.WriteLine($"Font index #{i}");
    Console.WriteLine($"\tName: {allFonts[i].Name}");
    Console.WriteLine($"\tIs {(allFonts[i].IsTrueType ? "" : "not ")}a trueType font");
}
```

### Смотрите также

* class [FontInfo](../)
* пространство имен [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* сборка [Aspose.Words](../../../)
