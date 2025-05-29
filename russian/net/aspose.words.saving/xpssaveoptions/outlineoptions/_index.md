---
title: XpsSaveOptions.OutlineOptions
linktitle: OutlineOptions
articleTitle: OutlineOptions
second_title: Aspose.Words для .NET
description: Откройте для себя свойство XpsSaveOptions OutlineOptions, позволяющее настраивать параметры структуры документа для улучшенной организации и представления.
type: docs
weight: 30
url: /ru/net/aspose.words.saving/xpssaveoptions/outlineoptions/
---
## XpsSaveOptions.OutlineOptions property

Позволяет указать параметры контура.

```csharp
public OutlineOptions OutlineOptions { get; }
```

## Примечания

Обратите внимание, что[`ExpandedOutlineLevels`](../../outlineoptions/expandedoutlinelevels/) опция не будет работать при сохранении в XPS.

## Примеры

Показывает, как ограничить уровень заголовков, которые будут отображаться в структуре сохраненного документа XPS.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставьте заголовки, которые могут служить записями оглавления уровней 1, 2 и 3.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;

Assert.True(builder.ParagraphFormat.IsHeading);

builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;

builder.Writeln("Heading 1.1");
builder.Writeln("Heading 1.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading3;

builder.Writeln("Heading 1.2.1");
builder.Writeln("Heading 1.2.2");

// Создаем объект "XpsSaveOptions", который можно передать методу "Save" документа
// чтобы изменить способ преобразования этим методом документа в .XPS.
XpsSaveOptions saveOptions = new XpsSaveOptions();

Assert.AreEqual(SaveFormat.Xps, saveOptions.SaveFormat);

// Выходной документ XPS будет содержать структуру, оглавление, в котором перечислены заголовки в тексте документа.
// Нажатие на запись в этой схеме перенесет нас к местоположению соответствующего заголовка.
// Установите свойство "HeadingsOutlineLevels" на "2", чтобы исключить из структуры все заголовки, уровни которых выше 2.
// Последние два заголовка, которые мы вставили выше, не появятся.
saveOptions.OutlineOptions.HeadingsOutlineLevels = 2;

doc.Save(ArtifactsDir + "XpsSaveOptions.OutlineLevels.xps", saveOptions);
```

### Смотрите также

* class [OutlineOptions](../../outlineoptions/)
* class [XpsSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
