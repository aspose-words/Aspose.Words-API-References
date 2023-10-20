---
title: RevisionTextEffect Enum
linktitle: RevisionTextEffect
articleTitle: RevisionTextEffect
second_title: Aspose.Words для .NET
description: Aspose.Words.Layout.RevisionTextEffect перечисление. Позволяет указать эффект оформления для редакций текста документа на С#.
type: docs
weight: 3400
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
| None | `0` | К переработанному содержимому не применяются специальные эффекты. Это соответствуетNoHighlight . |
| Color | `1` | Пересмотренный контент выделяется только цветом. |
| Bold | `2` | Пересмотренное содержимое выделено жирным шрифтом и цветным. |
| Italic | `3` | Пересмотренное содержимое выделено курсивом и цветным. |
| Underline | `4` | Отредактированное содержимое подчеркнуто и окрашено. |
| DoubleUnderline | `5` | Отредактированное содержимое подчеркнуто дважды и окрашено. |
| StrikeThrough | `6` | Отредактированное содержимое обведено и раскрашено. |
| DoubleStrikeThrough | `7` | Отредактированное содержимое обведено двойной обводкой и окрашено. |
| Hidden | `8` | Измененное содержимое скрыто. |

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

* пространство имен [Aspose.Words.Layout](../../aspose.words.layout/)
* сборка [Aspose.Words](../../)
