---
title: FieldAdvance.UpOffset
linktitle: UpOffset
articleTitle: UpOffset
second_title: Aspose.Words для .NET
description: Узнайте, как свойство FieldAdvance UpOffset улучшает позиционирование текста в ваших документах, сдвигая последующий текст вверх для получения изысканного вида.
type: docs
weight: 60
url: /ru/net/aspose.words.fields/fieldadvance/upoffset/
---
## FieldAdvance.UpOffset property

Возвращает или задает количество точек, на которое следует переместить вверх текст, следующий за полем.

```csharp
public string UpOffset { get; set; }
```

## Примеры

Показывает, как вставить поле ADVANCE и редактировать его свойства.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("This text is in its normal place.");

// Ниже приведены два способа использования поля ADVANCE для настройки положения текста, следующего за ним.
// Эффекты поля ADVANCE продолжают применяться до тех пор, пока не закончится абзац,
// или другое поле ADVANCE обновляет значения смещения/координат.
// 1 - Укажите смещение направления:
FieldAdvance field = (FieldAdvance)builder.InsertField(FieldType.FieldAdvance, true);
field.RightOffset = "5";
field.UpOffset = "5";

Assert.AreEqual(" ADVANCE  \\r 5 \\u 5", field.GetFieldCode());

builder.Write("This text will be moved up and to the right.");

field = (FieldAdvance)builder.InsertField(FieldType.FieldAdvance, true);
field.DownOffset = "5";
field.LeftOffset = "100";

Assert.AreEqual(" ADVANCE  \\d 5 \\l 100", field.GetFieldCode());

builder.Writeln("This text is moved down and to the left, overlapping the previous text.");

// 2 - Переместить текст в позицию, указанную координатами:
field = (FieldAdvance)builder.InsertField(FieldType.FieldAdvance, true);
field.HorizontalPosition = "-100";
field.VerticalPosition = "200";

Assert.AreEqual(" ADVANCE  \\x -100 \\y 200", field.GetFieldCode());

builder.Write("This text is in a custom position.");

doc.Save(ArtifactsDir + "Field.ADVANCE.docx");
```

### Смотрите также

* class [FieldAdvance](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
