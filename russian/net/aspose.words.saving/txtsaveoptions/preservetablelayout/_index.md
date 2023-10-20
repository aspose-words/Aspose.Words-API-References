---
title: TxtSaveOptions.PreserveTableLayout
linktitle: PreserveTableLayout
articleTitle: PreserveTableLayout
second_title: Aspose.Words для .NET
description: TxtSaveOptions PreserveTableLayout свойство. Указывает должна ли программа пытаться сохранить макет таблиц при сохранении в текстовом формате. Значение по умолчаниюЛОЖЬ  на С#.
type: docs
weight: 50
url: /ru/net/aspose.words.saving/txtsaveoptions/preservetablelayout/
---
## TxtSaveOptions.PreserveTableLayout property

Указывает, должна ли программа пытаться сохранить макет таблиц при сохранении в текстовом формате. Значение по умолчанию:`ЛОЖЬ` .

```csharp
public bool PreserveTableLayout { get; set; }
```

## Примеры

Показывает, как сохранить макет таблиц при преобразовании в открытый текст.

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

// Создаем объект «TxtSaveOptions», который мы можем передать методу «Save» документа.
// чтобы изменить способ сохранения документа в виде открытого текста.
TxtSaveOptions txtSaveOptions = new TxtSaveOptions();

// Установите для свойства PreserveTableLayout значение «true», чтобы применить к содержимому заполнение пробелами
// выходного открытого текстового документа, чтобы сохранить как можно большую часть макета таблицы.
// Установите для свойства PreserveTableLayout значение «false», чтобы сохранить содержимое всех таблиц
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
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
