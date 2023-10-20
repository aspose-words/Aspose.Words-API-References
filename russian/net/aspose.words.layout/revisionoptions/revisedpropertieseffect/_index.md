---
title: RevisionOptions.RevisedPropertiesEffect
linktitle: RevisedPropertiesEffect
articleTitle: RevisedPropertiesEffect
second_title: Aspose.Words для .NET
description: RevisionOptions RevisedPropertiesEffect свойство. Позволяет указать эффект для областей контента при изменении свойств форматирования.FormatChange Значение по умолчаниюNone на С#.
type: docs
weight: 120
url: /ru/net/aspose.words.layout/revisionoptions/revisedpropertieseffect/
---
## RevisionOptions.RevisedPropertiesEffect property

Позволяет указать эффект для областей контента при изменении свойств форматирования.FormatChange Значение по умолчанию:None

```csharp
public RevisionTextEffect RevisedPropertiesEffect { get; set; }
```

## Примечания

Hiddenне допускается и приведет кArgumentOutOfRangeException.

## Примеры

Показывает, как изменить внешний вид редакций.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

// Получаем объект RevisionOptions, который управляет внешним видом редакций.
RevisionOptions revisionOptions = doc.LayoutOptions.RevisionOptions;

// Отображение изменений вставки зеленым и курсивом.
revisionOptions.InsertedTextColor = RevisionColor.Green;
revisionOptions.InsertedTextEffect = RevisionTextEffect.Italic;

// Отобразить удаленные версии красным и жирным шрифтом.
revisionOptions.DeletedTextColor = RevisionColor.Red;
revisionOptions.DeletedTextEffect = RevisionTextEffect.Bold;

// Один и тот же текст появится дважды в версии движения:
// один раз в пункте отправления и один раз в пункте назначения.
// Отобразить текст в перенесенной из редакции желтого цвета с двойным перечеркиванием
// и двойное подчеркивание синим цветом в перенесенной версии.
revisionOptions.MovedFromTextColor = RevisionColor.Yellow;
revisionOptions.MovedFromTextEffect = RevisionTextEffect.DoubleStrikeThrough;
revisionOptions.MovedToTextColor = RevisionColor.ClassicBlue;
revisionOptions.MovedFromTextEffect = RevisionTextEffect.DoubleUnderline;

// Редакции формата отображаются темно-красным и жирным шрифтом.
revisionOptions.RevisedPropertiesColor = RevisionColor.DarkRed;
revisionOptions.RevisedPropertiesEffect = RevisionTextEffect.Bold;

// Размещаем толстую темно-синюю полосу в левой части страницы рядом со строками, на которые внесены изменения.
revisionOptions.RevisionBarsColor = RevisionColor.DarkBlue;
revisionOptions.RevisionBarsWidth = 15.0f;

// Показать отметки редакции и исходный текст.
revisionOptions.ShowOriginalRevision = true;
revisionOptions.ShowRevisionMarks = true;

// Получение перемещения, удаления, изменений форматирования и комментариев, которые будут отображаться в зеленых выносках
// в правой части страницы.
revisionOptions.ShowInBalloons = ShowInBalloons.Format;
revisionOptions.CommentColor = RevisionColor.BrightGreen;

// Эти функции применимы только к таким форматам, как .pdf или .jpg.
doc.Save(ArtifactsDir + "Revision.RevisionOptions.pdf");
```

### Смотрите также

* enum [RevisionTextEffect](../../revisiontexteffect/)
* class [RevisionOptions](../)
* пространство имен [Aspose.Words.Layout](../../../aspose.words.layout/)
* сборка [Aspose.Words](../../../)
