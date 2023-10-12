---
title: XpsSaveOptions.OutlineOptions
second_title: Справочник по API Aspose.Words для .NET
description: XpsSaveOptions свойство. Позволяет указать параметры контура.
type: docs
weight: 20
url: /ru/net/aspose.words.saving/xpssaveoptions/outlineoptions/
---
## XpsSaveOptions.OutlineOptions property

Позволяет указать параметры контура.

```csharp
public OutlineOptions OutlineOptions { get; }
```

### Примечания

Обратите внимание, что[`ExpandedOutlineLevels`](../../outlineoptions/expandedoutlinelevels/) опция не будет работать при сохранении в XPS.

### Примеры

Показывает, как ограничить уровень заголовков, которые будут отображаться в структуре сохраненного документа XPS.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставляем заголовки, которые могут служить записями оглавления уровней 1, 2, а затем 3.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;

Assert.True(builder.ParagraphFormat.IsHeading);

builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;

builder.Writeln("Heading 1.1");
builder.Writeln("Heading 1.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading3;

builder.Writeln("Heading 1.2.1");
builder.Writeln("Heading 1.2.2");

// Создаем объект «XpsSaveOptions», который мы можем передать методу «Save» документа.
// чтобы изменить способ преобразования этого метода в документ .XPS.
XpsSaveOptions saveOptions = new XpsSaveOptions();

Assert.AreEqual(SaveFormat.Xps, saveOptions.SaveFormat);

// Выходной документ XPS будет содержать структуру, оглавление, в котором перечислены заголовки в теле документа.
// Нажатие на запись в этом контуре приведет нас к местоположению соответствующего заголовка.
// Установите для свойства «HeadingsOutlineLevels» значение «2», чтобы исключить из структуры все заголовки, уровни которых выше 2.
// Последние два заголовка, которые мы вставили выше, не появятся.
saveOptions.OutlineOptions.HeadingsOutlineLevels = 2;

doc.Save(ArtifactsDir + "XpsSaveOptions.OutlineLevels.xps", saveOptions);
```

### Смотрите также

* class [OutlineOptions](../../outlineoptions/)
* class [XpsSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../xpssaveoptions/)
* сборка [Aspose.Words](../../../)


