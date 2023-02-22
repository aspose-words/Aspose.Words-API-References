---
title: Class RevisionOptions
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Layout.RevisionOptions сорт. Позволяет контролировать как обрабатываются версии документа в процессе компоновки.
type: docs
weight: 3190
url: /ru/net/aspose.words.layout/revisionoptions/
---
## RevisionOptions class

Позволяет контролировать, как обрабатываются версии документа в процессе компоновки.

```csharp
public class RevisionOptions
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [CommentColor](../../aspose.words.layout/revisionoptions/commentcolor/) { get; set; } | Позволяет указать цвет, который будет использоваться для комментариев. Значение по умолчанию:Red . |
| [DeletedTextColor](../../aspose.words.layout/revisionoptions/deletedtextcolor/) { get; set; } | Позволяет указать цвет, который будет использоваться для удаленного контента.Deletion . Значение по умолчанию:ByAuthor . |
| [DeletedTextEffect](../../aspose.words.layout/revisionoptions/deletedtexteffect/) { get; set; } | Позволяет указать эффект, который будет применяться к удаленному контентуDeletion . Значение по умолчанию:StrikeThrough |
| [InsertedTextColor](../../aspose.words.layout/revisionoptions/insertedtextcolor/) { get; set; } | Позволяет указать цвет, который будет использоваться для вставленного контентаInsertion . Значение по умолчанию:ByAuthor . |
| [InsertedTextEffect](../../aspose.words.layout/revisionoptions/insertedtexteffect/) { get; set; } | Позволяет указать эффект, который будет применяться к вставленному контентуInsertion . Значение по умолчанию:Underline . |
| [MeasurementUnit](../../aspose.words.layout/revisionoptions/measurementunit/) { get; set; } | Позволяет указать единицы измерения для комментариев к ревизии. Значение по умолчанию:Centimeters |
| [MovedFromTextColor](../../aspose.words.layout/revisionoptions/movedfromtextcolor/) { get; set; } | Позволяет указать цвет, который будет использоваться для областей, из которых было перемещено содержимое.Moving . Значение по умолчанию:ByAuthor . |
| [MovedFromTextEffect](../../aspose.words.layout/revisionoptions/movedfromtexteffect/) { get; set; } | Позволяет указать эффект, который будет применяться к областям, из которых был перемещен контентMoving . Значение по умолчанию:DoubleStrikeThrough |
| [MovedToTextColor](../../aspose.words.layout/revisionoptions/movedtotextcolor/) { get; set; } | Позволяет указать цвет, который будет использоваться для областей, в которые было перемещено содержимое.Moving . Значение по умолчанию:ByAuthor . |
| [MovedToTextEffect](../../aspose.words.layout/revisionoptions/movedtotexteffect/) { get; set; } | Позволяет указать эффект, который будет применяться к областям, куда был перемещен контентMoving . Значение по умолчанию:DoubleUnderline |
| [RevisedPropertiesColor](../../aspose.words.layout/revisionoptions/revisedpropertiescolor/) { get; set; } | Позволяет указать цвет, который будет использоваться для содержимого с изменением свойств форматирования.FormatChange Значение по умолчанию:NoHighlight . |
| [RevisedPropertiesEffect](../../aspose.words.layout/revisionoptions/revisedpropertieseffect/) { get; set; } | Позволяет указать эффект для областей содержимого с изменением свойств форматированияFormatChange Значение по умолчанию:None |
| [RevisionBarsColor](../../aspose.words.layout/revisionoptions/revisionbarscolor/) { get; set; } | Позволяет указать цвет, который будет использоваться для боковых полос, обозначающих строки документа, содержащие измененную информацию. Значение по умолчанию:Red . |
| [RevisionBarsPosition](../../aspose.words.layout/revisionoptions/revisionbarsposition/) { get; set; } | Получает или задает позицию визуализации штрихов изменений. Значение по умолчанию:Outside . |
| [RevisionBarsWidth](../../aspose.words.layout/revisionoptions/revisionbarswidth/) { get; set; } | Получает или задает ширину исправлений в пунктах. |
| [ShowInBalloons](../../aspose.words.layout/revisionoptions/showinballoons/) { get; set; } | Позволяет указать, будут ли ревизии отображаться во всплывающих подсказках. Значение по умолчанию:None . |
| [ShowOriginalRevision](../../aspose.words.layout/revisionoptions/showoriginalrevision/) { get; set; } | Позволяет указать, должен ли отображаться исходный текст вместо исправленного. Значение по умолчанию — False. |
| [ShowRevisionBars](../../aspose.words.layout/revisionoptions/showrevisionbars/) { get; set; } | Позволяет указать, следует ли отображать полосы изменений рядом со строками, содержащими исправленное содержимое. Значение по умолчанию — True. |
| [ShowRevisionMarks](../../aspose.words.layout/revisionoptions/showrevisionmarks/) { get; set; } | Позволяет указать, следует ли помечать текст редакции специальной разметкой форматирования. Значение по умолчанию — True. |

### Примеры

Показывает, как изменить внешний вид редакций в подготовленном к просмотру выходном документе.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставьте ревизию, затем измените цвет всех ревизий на зеленый.
builder.Writeln("This is not a revision.");
doc.StartTrackRevisions("John Doe", DateTime.Now);
builder.Writeln("This is a revision.");
doc.StopTrackRevisions();
builder.Writeln("This is not a revision.");

// Удаляем полосу, которая появляется слева от каждой исправленной строки.
doc.LayoutOptions.RevisionOptions.InsertedTextColor = RevisionColor.BrightGreen;
doc.LayoutOptions.RevisionOptions.ShowRevisionBars = false;

doc.Save(ArtifactsDir + "Document.LayoutOptionsRevisions.pdf");
```

### Смотрите также

* пространство имен [Aspose.Words.Layout](../../aspose.words.layout/)
* сборка [Aspose.Words](../../)


