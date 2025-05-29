---
title: MultiplePagesType Enum
linktitle: MultiplePagesType
articleTitle: MultiplePagesType
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.Settings.MultiplePagesType для эффективных вариантов печати документов. Оптимизируйте свой рабочий процесс с помощью гибких настроек печати!
type: docs
weight: 6700
url: /ru/net/aspose.words.settings/multiplepagestype/
---
## MultiplePagesType enumeration

Указывает, как документ будет распечатан.

```csharp
public enum MultiplePagesType
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Normal | `0` | Обычная печать, многостраничность не указана. |
| MirrorMargins | `1` | Меняет местами левое и правое поля на разворотах. |
| TwoPagesPerSheet | `2` | Печатает две страницы на листе. |
| BookFoldPrinting | `3` | Указывает, следует ли печатать документ в виде книжного сгиба. |
| BookFoldPrintingReverse | `4` | Указывает, следует ли печатать документ в виде перевернутой книжной фальцовки. |
| Default | `0` | Значение по умолчанию:Normal |

## Примеры

Показывает, как настроить документ, который можно напечатать в виде книжного сгиба.

```csharp
Document doc = new Document();

// Вставьте текст, занимающий 16 страниц.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("My Booklet:");

for (int i = 0; i < 15; i++)
{
    builder.InsertBreak(BreakType.PageBreak);
    builder.Write($"Booklet face #{i}");
}

// Настройте свойство «PageSetup» первого раздела для печати документа в виде книжного сгиба.
// Когда мы печатаем этот документ с обеих сторон, мы можем взять страницы и сложить их в стопку
// и сложите их все посередине одновременно. Содержимое документа выстроится в книжный сгиб.
PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.MultiplePages = MultiplePagesType.BookFoldPrinting;

// Мы можем указать только количество листов, кратное 4.
pageSetup.SheetsPerBooklet = 4;

doc.Save(ArtifactsDir + "PageSetup.Booklet.docx");
```

### Смотрите также

* пространство имен [Aspose.Words.Settings](../../aspose.words.settings/)
* сборка [Aspose.Words](../../)
