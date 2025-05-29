---
title: RevisionOptions.ShowRevisionMarks
linktitle: ShowRevisionMarks
articleTitle: ShowRevisionMarks
second_title: Aspose.Words для .NET
description: Управляйте видимостью ревизий с помощью свойства ShowRevisionMarks. Легко форматируйте текст ревизий для ясности, улучшая совместную работу с документами. Значение по умолчанию — true.
type: docs
weight: 210
url: /ru/net/aspose.words.layout/revisionoptions/showrevisionmarks/
---
## RevisionOptions.ShowRevisionMarks property

Позволяет указать, следует ли помечать текст редакции специальной разметкой форматирования. Значение по умолчанию:`истинный` .

```csharp
public bool ShowRevisionMarks { get; set; }
```

## Примеры

Показывает, как изменить внешний вид ревизий.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

// Получить объект RevisionOptions, который управляет внешним видом ревизий.
RevisionOptions revisionOptions = doc.LayoutOptions.RevisionOptions;

// Выделить исправления вставки зеленым курсивом.
revisionOptions.InsertedTextColor = RevisionColor.Green;
revisionOptions.InsertedTextEffect = RevisionTextEffect.Italic;

// Выделить удаленные ревизии красным и жирным шрифтом.
revisionOptions.DeletedTextColor = RevisionColor.Red;
revisionOptions.DeletedTextEffect = RevisionTextEffect.Bold;

// Один и тот же текст будет появляться дважды в редакции движения:
// один раз в пункте отправления и один раз в пункте прибытия.
// Отобразить текст в ревизии, из которой был перемещен, желтым с двойным зачеркиванием
// и дважды подчеркнута синим цветом в месте, куда перенесена редакция.
revisionOptions.MovedFromTextColor = RevisionColor.Yellow;
revisionOptions.MovedFromTextEffect = RevisionTextEffect.DoubleStrikeThrough;
revisionOptions.MovedToTextColor = RevisionColor.ClassicBlue;
revisionOptions.MovedToTextEffect = RevisionTextEffect.DoubleUnderline;

// Выделите изменения формата темно-красным и жирным шрифтом.
revisionOptions.RevisedPropertiesColor = RevisionColor.DarkRed;
revisionOptions.RevisedPropertiesEffect = RevisionTextEffect.Bold;

// Разместите толстую темно-синюю полосу в левой части страницы рядом со строками, затронутыми изменениями.
revisionOptions.RevisionBarsColor = RevisionColor.DarkBlue;
revisionOptions.RevisionBarsWidth = 15.0f;

// Показать исправленные отметки и исходный текст.
revisionOptions.ShowOriginalRevision = true;
revisionOptions.ShowRevisionMarks = true;

// Отображение перемещений, удалений, изменений форматирования и комментариев в зеленых шариках
// на правой стороне страницы.
revisionOptions.ShowInBalloons = ShowInBalloons.Format;
revisionOptions.CommentColor = RevisionColor.BrightGreen;

// Эти функции применимы только к таким форматам, как .pdf или .jpg.
doc.Save(ArtifactsDir + "Revision.RevisionOptions.pdf");
```

### Смотрите также

* class [RevisionOptions](../)
* пространство имен [Aspose.Words.Layout](../../../aspose.words.layout/)
* сборка [Aspose.Words](../../../)
