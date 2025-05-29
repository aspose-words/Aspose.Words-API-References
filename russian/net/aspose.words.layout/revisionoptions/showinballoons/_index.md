---
title: RevisionOptions.ShowInBalloons
linktitle: ShowInBalloons
articleTitle: ShowInBalloons
second_title: Aspose.Words для .NET
description: Откройте для себя свойство RevisionOptions ShowInBalloons! Управляйте видимостью ревизий в выносках для повышения ясности документа. По умолчанию — None.
type: docs
weight: 180
url: /ru/net/aspose.words.layout/revisionoptions/showinballoons/
---
## RevisionOptions.ShowInBalloons property

Позволяет указать, будут ли ревизии отображаться в выносках. Значение по умолчанию:None .

```csharp
public ShowInBalloons ShowInBalloons { get; set; }
```

## Примечания

Обратите внимание, что изменения не отображаются в виде всплывающих окон дляShowInAnnotations .

## Примеры

Показывает, как отображать изменения в выносках.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

// По умолчанию текст, являющийся ревизией, имеет другой цвет, чтобы отличить его от остального текста, не являющегося ревизией.
// Установите параметр ревизии, чтобы отображать более подробную информацию о каждой ревизии в выноске на правом поле страницы.
doc.LayoutOptions.RevisionOptions.ShowInBalloons = ShowInBalloons.FormatAndDelete;
doc.Save(ArtifactsDir + "Revision.ShowRevisionBalloons.pdf");
```

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

* enum [ShowInBalloons](../../showinballoons/)
* class [RevisionOptions](../)
* пространство имен [Aspose.Words.Layout](../../../aspose.words.layout/)
* сборка [Aspose.Words](../../../)
