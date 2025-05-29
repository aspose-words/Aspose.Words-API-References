---
title: TxtSaveOptions.PreserveTableLayout
linktitle: PreserveTableLayout
articleTitle: PreserveTableLayout
second_title: Aspose.Words для .NET
description: Откройте для себя функцию PreserveTableLayout TxtSaveOptions, которая гарантирует сохранение макета таблиц при сохранении в виде обычного текста. Улучшите читаемость документа!
type: docs
weight: 50
url: /ru/net/aspose.words.saving/txtsaveoptions/preservetablelayout/
---
## TxtSaveOptions.PreserveTableLayout property

Указывает, должна ли программа пытаться сохранить расположение таблиц при сохранении в формате простого текста. Значение по умолчанию:`ЛОЖЬ` .

```csharp
public bool PreserveTableLayout { get; set; }
```

## Примеры

Показывает, как сохранить структуру таблиц при преобразовании в обычный текст.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, cell 1");
builder.InsertCell();
builder.Write("Row 1, cell 2");
builder.EndRow();
builder.InsertCell();
builder.Write("Row 2, cell 1");
builder.InsertCell();
builder.Write("Row 2, cell 2");
builder.EndTable();

// Создаем объект "TxtSaveOptions", который можно передать методу "Save" документа
// чтобы изменить способ сохранения документа в виде обычного текста.
TxtSaveOptions txtSaveOptions = new TxtSaveOptions();

// Установите свойство "PreserveTableLayout" в значение "true", чтобы применить пробельные отступы к содержимому
// выходного текстового документа, чтобы сохранить как можно больше макета таблицы.
// Установите свойство "PreserveTableLayout" в значение "false", чтобы сохранить содержимое всех таблиц
// как непрерывный текст, с новой строкой для каждой строки.
txtSaveOptions.PreserveTableLayout = preserveTableLayout;

doc.Save(ArtifactsDir + "TxtSaveOptions.PreserveTableLayout.txt", txtSaveOptions);

string docText = File.ReadAllText(ArtifactsDir + "TxtSaveOptions.PreserveTableLayout.txt");

if (preserveTableLayout)
    Assert.AreEqual("Row 1, cell 1                                            Row 1, cell 2\r\n" +
                    "Row 2, cell 1                                            Row 2, cell 2\r\n\r\n", docText);
else
    Assert.AreEqual("Row 1, cell 1\r" +
                    "Row 1, cell 2\r" +
                    "Row 2, cell 1\r" +
                    "Row 2, cell 2\r\r\n", docText);
```

### Смотрите также

* class [TxtSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
