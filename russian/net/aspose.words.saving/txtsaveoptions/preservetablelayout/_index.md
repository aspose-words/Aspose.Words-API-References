---
title: TxtSaveOptions.PreserveTableLayout
second_title: Справочник по API Aspose.Words для .NET
description: TxtSaveOptions свойство. Указывает должна ли программа сохранять расположение таблиц при сохранении в текстовом формате. Значение по умолчанию ЛОЖЬ .
type: docs
weight: 50
url: /ru/net/aspose.words.saving/txtsaveoptions/preservetablelayout/
---
## TxtSaveOptions.PreserveTableLayout property

Указывает, должна ли программа сохранять расположение таблиц при сохранении в текстовом формате. Значение по умолчанию: **ЛОЖЬ** .

```csharp
public bool PreserveTableLayout { get; set; }
```

### Примеры

Показывает, как сохранить макет таблиц при преобразовании в обычный текст.

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

// Создаем объект "TxtSaveOptions", который мы можем передать в метод "Сохранить" документа
// чтобы изменить способ сохранения документа в виде открытого текста.
TxtSaveOptions txtSaveOptions = new TxtSaveOptions();

// Установите для свойства "PreserveTableLayout" значение "true", чтобы применить заполнение пробелами к содержимому
// выходного документа с открытым текстом, чтобы сохранить как можно большую часть макета таблицы.
// Установите для свойства "PreserveTableLayout" значение "false", чтобы сохранить содержимое всех таблиц
// как непрерывный текст, только с новой строкой для каждой строки.
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
* пространство имен [Aspose.Words.Saving](../../txtsaveoptions/)
* сборка [Aspose.Words](../../../)


