---
title: TxtSaveOptionsBase.ForcePageBreaks
linktitle: ForcePageBreaks
articleTitle: ForcePageBreaks
second_title: Aspose.Words для .NET
description: Контролируйте разрывы страниц с помощью свойства ForcePageBreaks TxtSaveOptionsBase. Обеспечьте бесперебойный экспорт и сохраняйте форматирование документа без усилий.
type: docs
weight: 30
url: /ru/net/aspose.words.saving/txtsaveoptionsbase/forcepagebreaks/
---
## TxtSaveOptionsBase.ForcePageBreaks property

Позволяет указать, следует ли сохранять разрывы страниц при экспорте.

Значение по умолчанию:`ЛОЖЬ`.

```csharp
public bool ForcePageBreaks { get; set; }
```

## Примечания

Свойство влияет только на разрывы страниц, которые явно вставлены в документ. Оно не связано с разрывами страниц, которые MS Word автоматически вставляет в конце каждой страницы.

## Примеры

Показывает, как указать, следует ли сохранять разрывы страниц при экспорте документа в обычный текст.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Page 1");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3");

// Создаем объект "TxtSaveOptions", который можно передать в функцию "Сохранить" документа
// метод для изменения способа сохранения документа в виде обычного текста.
TxtSaveOptions saveOptions = new TxtSaveOptions();

// Объекты Aspose.Words «Документ» имеют разрывы страниц, как и документы Microsoft Word.
// Форматы сохранения, такие как «.txt», представляют собой единый непрерывный текст без разрывов страниц.
// Установите свойство «ForcePageBreaks» в значение «true», чтобы сохранить все разрывы страниц в виде символов '\f'.
// Установите свойство «ForcePageBreaks» в значение «false», чтобы отменить все разрывы страниц.
saveOptions.ForcePageBreaks = forcePageBreaks;

doc.Save(ArtifactsDir + "TxtSaveOptions.PageBreaks.txt", saveOptions);

// Если мы загрузим текстовый документ с разрывами страниц,
// объект «Документ» будет использовать их для разделения тела на страницы.
doc = new Document(ArtifactsDir + "TxtSaveOptions.PageBreaks.txt");

Assert.AreEqual(forcePageBreaks ? 3 : 1, doc.PageCount);
```

### Смотрите также

* class [TxtSaveOptionsBase](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
