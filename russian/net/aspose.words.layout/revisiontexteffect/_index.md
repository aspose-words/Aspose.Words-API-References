---
title: RevisionTextEffect Enum
linktitle: RevisionTextEffect
articleTitle: RevisionTextEffect
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.Layout.RevisionTextEffect, чтобы улучшить ревизии документов с помощью уникальных эффектов оформления текста. Повысьте свой опыт редактирования!
type: docs
weight: 3850
url: /ru/net/aspose.words.layout/revisiontexteffect/
---
## RevisionTextEffect enumeration

Позволяет указать эффект оформления для редакций текста документа.

```csharp
public enum RevisionTextEffect
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| None | `0` | Измененный контент не имеет примененных спецэффектов. Это соответствуетNoHighlight . |
| Color | `1` | Измененное содержимое выделено только цветом. |
| Bold | `2` | Измененное содержание выделено жирным шрифтом и цветом. |
| Italic | `3` | Измененное содержимое выделено курсивом и цветом. |
| Underline | `4` | Измененное содержание подчеркнуто и закрашено. |
| DoubleUnderline | `5` | Измененное содержание подчеркнуто дважды и выделено цветом. |
| StrikeThrough | `6` | Измененное содержимое заштриховано и окрашено. |
| DoubleStrikeThrough | `7` | Измененное содержимое зачеркнуто и окрашено. |
| Hidden | `8` | Измененный контент скрыт. |

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

* пространство имен [Aspose.Words.Layout](../../aspose.words.layout/)
* сборка [Aspose.Words](../../)
