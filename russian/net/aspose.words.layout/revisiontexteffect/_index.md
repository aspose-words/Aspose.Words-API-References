---
title: Enum RevisionTextEffect
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Layout.RevisionTextEffect перечисление. Позволяет указать эффект оформления для редакций текста документа.
type: docs
weight: 3200
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
| None | `0` | В исправленном контенте не применяются специальные эффекты. Это соответствуетNoHighlight . |
| Color | `1` | Измененный контент выделяется только цветом. |
| Bold | `2` | Измененное содержимое выделено жирным шрифтом и окрашено. |
| Italic | `3` | Измененное содержимое выделено курсивом и окрашено. |
| Underline | `4` | Измененное содержимое подчеркнуто и окрашено. |
| DoubleUnderline | `5` | Измененное содержимое выделено двойным подчеркиванием и окрашено. |
| StrikeThrough | `6` | Пересмотренный контент зачеркнут и окрашен. |
| DoubleStrikeThrough | `7` | Измененный контент зачеркнут двойным штрихом и окрашен. |
| Hidden | `8` | Измененное содержимое скрыто. |

### Примеры

Показывает, как изменить внешний вид редакций.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

// Получить объект RevisionOptions, управляющий внешним видом ревизий.
RevisionOptions revisionOptions = doc.LayoutOptions.RevisionOptions;

// Отображение ревизий вставки зеленым цветом и курсивом.
revisionOptions.InsertedTextColor = RevisionColor.Green;
revisionOptions.InsertedTextEffect = RevisionTextEffect.Italic;

// Отображение удаленных ревизий красным и полужирным шрифтом.
revisionOptions.DeletedTextColor = RevisionColor.Red;
revisionOptions.DeletedTextEffect = RevisionTextEffect.Bold;

// Один и тот же текст появится дважды в ревизии движения:
// один раз в пункте отправления и один раз в пункте прибытия.
// Визуализируем текст перемещенной версии желтым цветом с двойным перечеркиванием
// и дважды подчеркнутый синим цветом ревизию, к которой был перемещен.
revisionOptions.MovedFromTextColor = RevisionColor.Yellow;
revisionOptions.MovedFromTextEffect = RevisionTextEffect.DoubleStrikeThrough;
revisionOptions.MovedToTextColor = RevisionColor.Blue;
revisionOptions.MovedFromTextEffect = RevisionTextEffect.DoubleUnderline;

// Редактирование формата темно-красным и полужирным шрифтом.
revisionOptions.RevisedPropertiesColor = RevisionColor.DarkRed;
revisionOptions.RevisedPropertiesEffect = RevisionTextEffect.Bold;

// Поместите толстую темно-синюю полосу в левой части страницы рядом со строками, затронутыми изменениями.
revisionOptions.RevisionBarsColor = RevisionColor.DarkBlue;
revisionOptions.RevisionBarsWidth = 15.0f;

// Показать метки исправления и исходный текст.
revisionOptions.ShowOriginalRevision = true;
revisionOptions.ShowRevisionMarks = true;

// Получить перемещение, удаление, исправления форматирования и комментарии для отображения в зеленых выносках
// в правой части страницы.
revisionOptions.ShowInBalloons = ShowInBalloons.Format;
revisionOptions.CommentColor = RevisionColor.BrightGreen;

// Эти функции применимы только к таким форматам, как .pdf или .jpg.
doc.Save(ArtifactsDir + "Revision.RevisionOptions.pdf");
```

### Смотрите также

* пространство имен [Aspose.Words.Layout](../../aspose.words.layout/)
* сборка [Aspose.Words](../../)


