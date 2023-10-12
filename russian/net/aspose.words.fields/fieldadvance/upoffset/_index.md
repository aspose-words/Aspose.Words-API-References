---
title: FieldAdvance.UpOffset
second_title: Справочник по API Aspose.Words для .NET
description: FieldAdvance свойство. Получает или задает количество пунктов на которое текст следующий за полем должен быть перемещен вверх.
type: docs
weight: 60
url: /ru/net/aspose.words.fields/fieldadvance/upoffset/
---
## FieldAdvance.UpOffset property

Получает или задает количество пунктов, на которое текст, следующий за полем, должен быть перемещен вверх.

```csharp
public string UpOffset { get; set; }
```

### Примеры

Показывает, как вставить поле ADVANCE и отредактировать его свойства.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("This text is in its normal place.");

// Ниже приведены два способа использования поля ADVANCE для настройки положения следующего за ним текста.
// Эффекты поля ADVANCE продолжают применяться до тех пор, пока не закончится абзац,
// или другое поле ADVANCE обновляет значения смещения/координаты.
// 1 - Укажите смещение по направлению:
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
* пространство имен [Aspose.Words.Fields](../../fieldadvance/)
* сборка [Aspose.Words](../../../)


