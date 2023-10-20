---
title: TxtSaveOptions.ListIndentation
linktitle: ListIndentation
articleTitle: ListIndentation
second_title: Aspose.Words для .NET
description: TxtSaveOptions ListIndentation свойство. ПолучаетTxtListIndentation объект который определяет сколько и какой символ использовать для отступов уровней списка. По умолчанию это нулевое количество символов 0 что означает отсутствие отступов на С#.
type: docs
weight: 30
url: /ru/net/aspose.words.saving/txtsaveoptions/listindentation/
---
## TxtSaveOptions.ListIndentation property

Получает[`TxtListIndentation`](../../txtlistindentation/) объект, который определяет, сколько и какой символ использовать для отступов уровней списка. По умолчанию это нулевое количество символов '\0', что означает отсутствие отступов.

```csharp
public TxtListIndentation ListIndentation { get; }
```

## Примеры

Показывает, как настроить отступ списка при сохранении документа в виде открытого текста.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Создаем список с тремя уровнями отступов.
builder.ListFormat.ApplyNumberDefault();
builder.Writeln("Item 1");
builder.ListFormat.ListIndent();
builder.Writeln("Item 2");
builder.ListFormat.ListIndent(); 
builder.Write("Item 3");

// Создаем объект «TxtSaveOptions», который мы можем передать методу «Save» документа.
// чтобы изменить способ сохранения документа в виде открытого текста.
TxtSaveOptions txtSaveOptions = new TxtSaveOptions();

// Установите свойство «Символ», чтобы назначить используемый символ
// для заполнения, имитирующего отступ списка в открытом тексте.
txtSaveOptions.ListIndentation.Character = ' ';

// Установите свойство «Count», чтобы указать количество раз
// для размещения символа заполнения для каждого уровня отступа списка.
txtSaveOptions.ListIndentation.Count = 3;

doc.Save(ArtifactsDir + "TxtSaveOptions.TxtListIndentation.txt", txtSaveOptions);

string docText = File.ReadAllText(ArtifactsDir + "TxtSaveOptions.TxtListIndentation.txt");

Assert.AreEqual("1. Item 1\r\n" +
                "   a. Item 2\r\n" +
                "      i. Item 3\r\n", docText);
```

### Смотрите также

* class [TxtListIndentation](../../txtlistindentation/)
* class [TxtSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
