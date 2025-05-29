---
title: FontInfo.IsTrueType
linktitle: IsTrueType
articleTitle: IsTrueType
second_title: Aspose.Words для .NET
description: Откройте для себя свойство FontInfo IsTrueType, гарантирующее, что ваш шрифт имеет тип TrueType или OpenType, что обеспечивает превосходное качество и идеально подходит для четких и масштабируемых дизайнов.
type: docs
weight: 50
url: /ru/net/aspose.words.fonts/fontinfo/istruetype/
---
## FontInfo.IsTrueType property

Указывает, что этот шрифт является шрифтом TrueType или OpenType, а не растровым или векторным шрифтом. Значение по умолчанию:`истинный` .

```csharp
public bool IsTrueType { get; set; }
```

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
