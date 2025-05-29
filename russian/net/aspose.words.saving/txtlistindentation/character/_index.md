---
title: TxtListIndentation.Character
linktitle: Character
articleTitle: Character
second_title: Aspose.Words для .NET
description: Откройте для себя свойство TxtListIndentation, чтобы настроить отступ списка с помощью предпочитаемого вами символа. Улучшите читаемость и визуальную привлекательность без усилий!
type: docs
weight: 20
url: /ru/net/aspose.words.saving/txtlistindentation/character/
---
## TxtListIndentation.Character property

Возвращает или задает символ, который следует использовать для отступа уровней списка. Значение по умолчанию — '\0', что означает отсутствие отступа.

```csharp
public char Character { get; set; }
```

## Примеры

Показывает, как настроить отступ списка при сохранении документа в виде обычного текста.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Создаем список с тремя уровнями отступа.
builder.ListFormat.ApplyNumberDefault();
builder.Writeln("Item 1");
builder.ListFormat.ListIndent();
builder.Writeln("Item 2");
builder.ListFormat.ListIndent(); 
builder.Write("Item 3");

// Создаем объект "TxtSaveOptions", который можно передать методу "Save" документа
// чтобы изменить способ сохранения документа в виде обычного текста.
TxtSaveOptions txtSaveOptions = new TxtSaveOptions();

// Установите свойство "Character", чтобы назначить символ для использования
// для заполнения, имитирующего отступ списка в открытом тексте.
txtSaveOptions.ListIndentation.Character = ' ';

// Установите свойство «Count», чтобы указать количество раз
// для размещения символа заполнения для каждого уровня отступа списка.
txtSaveOptions.ListIndentation.Count = 3;

doc.Save(ArtifactsDir + "TxtSaveOptions.TxtListIndentation.txt", txtSaveOptions);

string docText = File.ReadAllText(ArtifactsDir + "TxtSaveOptions.TxtListIndentation.txt");
string newLine= Environment.NewLine;

Assert.AreEqual($"1. Item 1{newLine}" +
                $"   a. Item 2{newLine}" +
                $"      i. Item 3{newLine}", docText);
```

### Смотрите также

* class [TxtListIndentation](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
