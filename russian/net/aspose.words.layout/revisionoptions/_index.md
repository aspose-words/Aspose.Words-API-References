---
title: RevisionOptions Class
linktitle: RevisionOptions
articleTitle: RevisionOptions
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Layout.RevisionOptions, который поможет вам эффективно управлять изменениями документов и улучшить процесс макетирования для достижения оптимальных результатов.
type: docs
weight: 3840
url: /ru/net/aspose.words.layout/revisionoptions/
---
## RevisionOptions class

Позволяет контролировать обработку изменений документа в процессе макетирования.

Чтобы узнать больше, посетите[Преобразование в формат с фиксированным размером страницы](https://docs.aspose.com/words/net/converting-to-fixed-page-format/) документальная статья.

```csharp
public class RevisionOptions
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [CommentColor](../../aspose.words.layout/revisionoptions/commentcolor/) { get; set; } | Позволяет указать цвет, который будет использоваться для комментариев. Значение по умолчанию:Red . |
| [DeleteCellColor](../../aspose.words.layout/revisionoptions/deletecellcolor/) { get; set; } | Позволяет указать цвет, который будет использоваться для удаленных ячеек.Deletion . Значение по умолчанию:Pink . |
| [DeletedTextColor](../../aspose.words.layout/revisionoptions/deletedtextcolor/) { get; set; } | Позволяет указать цвет, который будет использоваться для удаленного контента.Deletion . Значение по умолчанию:ByAuthor . |
| [DeletedTextEffect](../../aspose.words.layout/revisionoptions/deletedtexteffect/) { get; set; } | Позволяет указать эффект, который будет применен к удаленному контентуDeletion . Значение по умолчанию:StrikeThrough |
| [InsertCellColor](../../aspose.words.layout/revisionoptions/insertcellcolor/) { get; set; } | Позволяет указать цвет, который будет использоваться для вставленных ячеек.Insertion . Значение по умолчанию:Blue . |
| [InsertedTextColor](../../aspose.words.layout/revisionoptions/insertedtextcolor/) { get; set; } | Позволяет указать цвет, который будет использоваться для вставленного содержимогоInsertion . Значение по умолчанию:ByAuthor . |
| [InsertedTextEffect](../../aspose.words.layout/revisionoptions/insertedtexteffect/) { get; set; } | Позволяет указать эффект, который будет применен к вставленному контентуInsertion . Значение по умолчанию:Underline . |
| [MeasurementUnit](../../aspose.words.layout/revisionoptions/measurementunit/) { get; set; } | Позволяет указать единицы измерения для комментариев к ревизии. Значение по умолчанию:Centimeters |
| [MovedFromTextColor](../../aspose.words.layout/revisionoptions/movedfromtextcolor/) { get; set; } | Позволяет указать цвет, который будет использоваться для областей, из которых был перемещен контент.Moving . Значение по умолчанию:ByAuthor . |
| [MovedFromTextEffect](../../aspose.words.layout/revisionoptions/movedfromtexteffect/) { get; set; } | Позволяет указать эффект, который будет применен к областям, из которых был перемещен контентMoving . Значение по умолчанию:DoubleStrikeThrough |
| [MovedToTextColor](../../aspose.words.layout/revisionoptions/movedtotextcolor/) { get; set; } | Позволяет указать цвет, который будет использоваться для областей, куда был перемещен контентMoving . Значение по умолчанию:ByAuthor . |
| [MovedToTextEffect](../../aspose.words.layout/revisionoptions/movedtotexteffect/) { get; set; } | Позволяет указать эффект, который будет применен к областям, куда был перемещен контентMoving . Значение по умолчанию:DoubleUnderline |
| [RevisedPropertiesColor](../../aspose.words.layout/revisionoptions/revisedpropertiescolor/) { get; set; } | Позволяет указать цвет, который будет использоваться для содержимого при изменении свойств форматирования.FormatChange Значение по умолчанию:NoHighlight . |
| [RevisedPropertiesEffect](../../aspose.words.layout/revisionoptions/revisedpropertieseffect/) { get; set; } | Позволяет указать эффект для областей содержимого при изменении свойств форматированияFormatChange Значение по умолчанию:None |
| [RevisionBarsColor](../../aspose.words.layout/revisionoptions/revisionbarscolor/) { get; set; } | Позволяет указать цвет, который будет использоваться для боковых полос, обозначающих строки документа, содержащие измененную информацию. Значение по умолчанию:Red . |
| [RevisionBarsPosition](../../aspose.words.layout/revisionoptions/revisionbarsposition/) { get; set; } | Возвращает или задает позицию визуализации ревизионных полос. Значение по умолчанию:Outside . |
| [RevisionBarsWidth](../../aspose.words.layout/revisionoptions/revisionbarswidth/) { get; set; } | Возвращает или задает ширину ревизионных полос, точек. |
| [ShowInBalloons](../../aspose.words.layout/revisionoptions/showinballoons/) { get; set; } | Позволяет указать, будут ли ревизии отображаться в выносках. Значение по умолчанию:None . |
| [ShowOriginalRevision](../../aspose.words.layout/revisionoptions/showoriginalrevision/) { get; set; } | Позволяет указать, следует ли отображать исходный текст вместо измененного. Значение по умолчанию:`ЛОЖЬ` . |
| [ShowRevisionBars](../../aspose.words.layout/revisionoptions/showrevisionbars/) { get; set; } | Позволяет указать, следует ли отображать полосы исправлений рядом со строками, содержащими измененное содержимое. Значение по умолчанию:`истинный` . |
| [ShowRevisionMarks](../../aspose.words.layout/revisionoptions/showrevisionmarks/) { get; set; } | Позволяет указать, следует ли помечать текст редакции специальной разметкой форматирования. Значение по умолчанию:`истинный` . |

## Примеры

Показывает, как изменить внешний вид изменений в визуализированном выходном документе.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставьте ревизию, затем измените цвет всех ревизий на зеленый.
builder.Writeln("This is not a revision.");
doc.StartTrackRevisions("John Doe", DateTime.Now);
builder.Writeln("This is a revision.");
doc.StopTrackRevisions();
builder.Writeln("This is not a revision.");

// Удалить полосу, которая появляется слева от каждой измененной строки.
doc.LayoutOptions.RevisionOptions.InsertedTextColor = RevisionColor.BrightGreen;
doc.LayoutOptions.RevisionOptions.ShowRevisionBars = false;
doc.LayoutOptions.RevisionOptions.RevisionBarsPosition = HorizontalAlignment.Right;

doc.Save(ArtifactsDir + "Revision.LayoutOptionsRevisions.pdf");
```

### Смотрите также

* пространство имен [Aspose.Words.Layout](../../aspose.words.layout/)
* сборка [Aspose.Words](../../)
