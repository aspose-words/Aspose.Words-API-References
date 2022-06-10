---
title: ShowInBalloons
second_title: Справочник по API Aspose.Words для .NET
description: Позволяет указать отображаются ли ревизии во всплывающих подсказках. Значение по умолчаниюNone.
type: docs
weight: 160
url: /ru/net/aspose.words.layout/revisionoptions/showinballoons/
---
## RevisionOptions.ShowInBalloons property

Позволяет указать, отображаются ли ревизии во всплывающих подсказках. Значение по умолчанию:None.

```csharp
public ShowInBalloons ShowInBalloons { get; set; }
```

### Примечания

Обратите внимание, что исправления не отображаются в выносках дляShowInAnnotations.

### Примеры

Показывает, как отображать ревизии во всплывающих подсказках.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

 // Получить объект RevisionOptions, управляющий внешним видом ревизий.
RevisionOptions revisionOptions = doc.LayoutOptions.RevisionOptions;

 // Отображение ревизий вставки зеленым цветом и курсивом.
revisionOptions.InsertedTextColor = RevisionColor.Green;
revisionOptions.InsertedTextEffect = RevisionTextEffect.Italic;

 // Отображаем ревизии удаления красным и полужирным шрифтом.
revisionOptions.DeletedTextColor = RevisionColor.Red;
revisionOptions.DeletedTextEffect = RevisionTextEffect.Bold;

 // Один и тот же текст появится дважды в версии механизма: 
 // один раз в пункте отправления и один раз в пункте прибытия.
 // Визуализировать текст перемещенной версии желтым цветом с двойным перечеркиванием через
 // и двойное подчеркивание синего цвета на перемещенной ревизии.
revisionOptions.MovedFromTextColor = RevisionColor.Yellow;
revisionOptions.MovedFromTextEffect = RevisionTextEffect.DoubleStrikeThrough;
revisionOptions.MovedToTextColor = RevisionColor.Blue;
revisionOptions.MovedFromTextEffect = RevisionTextEffect.DoubleUnderline;

// Версии формата отображаются темно-красным и полужирным шрифтом.
revisionOptions.RevisedPropertiesColor = RevisionColor.DarkRed;
revisionOptions.RevisedPropertiesEffect = RevisionTextEffect.Bold;

 // Поместите толстую темно-синюю полосу в левой части страницы рядом со строками, затронутыми ревизиями.
revisionOptions.RevisionBarsColor = RevisionColor.DarkBlue;
revisionOptions.RevisionBarsWidth = 15.0f;

 // Показать метки исправления и исходный текст.
revisionOptions.ShowOriginalRevision = true;
revisionOptions.ShowRevisionMarks = true;

 // Получение изменений перемещения, удаления, форматирования и комментариев для отображения зелеными выносками
 // в правой части страницы.
revisionOptions.ShowInBalloons = ShowInBalloons.Format;
revisionOptions.CommentColor = RevisionColor.BrightGreen;

 // Эти функции применимы только к таким форматам, как .pdf или .jpg.
doc.Save(ArtifactsDir + "Revision.RevisionOptions.pdf");
```

Показывает, как изменить внешний вид ревизий.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

 // Получить объект RevisionOptions, управляющий внешним видом ревизий.
RevisionOptions revisionOptions = doc.LayoutOptions.RevisionOptions;

 // Отображение ревизий вставки зеленым цветом и курсивом.
revisionOptions.InsertedTextColor = RevisionColor.Green;
revisionOptions.InsertedTextEffect = RevisionTextEffect.Italic;

 // Отображаем ревизии удаления красным и полужирным шрифтом.
revisionOptions.DeletedTextColor = RevisionColor.Red;
revisionOptions.DeletedTextEffect = RevisionTextEffect.Bold;

 // Один и тот же текст появится дважды в версии механизма: 
 // один раз в пункте отправления и один раз в пункте прибытия.
 // Визуализировать текст перемещенной версии желтым цветом с двойным перечеркиванием через
 // и двойное подчеркивание синего цвета на перемещенной ревизии.
revisionOptions.MovedFromTextColor = RevisionColor.Yellow;
revisionOptions.MovedFromTextEffect = RevisionTextEffect.DoubleStrikeThrough;
revisionOptions.MovedToTextColor = RevisionColor.Blue;
revisionOptions.MovedFromTextEffect = RevisionTextEffect.DoubleUnderline;

// Версии формата отображаются темно-красным и полужирным шрифтом.
revisionOptions.RevisedPropertiesColor = RevisionColor.DarkRed;
revisionOptions.RevisedPropertiesEffect = RevisionTextEffect.Bold;

 // Поместите толстую темно-синюю полосу в левой части страницы рядом со строками, затронутыми ревизиями.
revisionOptions.RevisionBarsColor = RevisionColor.DarkBlue;
revisionOptions.RevisionBarsWidth = 15.0f;

 // Показать метки исправления и исходный текст.
revisionOptions.ShowOriginalRevision = true;
revisionOptions.ShowRevisionMarks = true;

 // Получение изменений перемещения, удаления, форматирования и комментариев для отображения зелеными выносками
 // в правой части страницы.
revisionOptions.ShowInBalloons = ShowInBalloons.Format;
revisionOptions.CommentColor = RevisionColor.BrightGreen;

 // Эти функции применимы только к таким форматам, как .pdf или .jpg.
doc.Save(ArtifactsDir + "Revision.RevisionOptions.pdf");
```

### Смотрите также

* enum [ShowInBalloons](../../showinballoons)
* class [RevisionOptions](../../revisionoptions)
* пространство имен [Aspose.Words.Layout](../../revisionoptions)
* сборка [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
