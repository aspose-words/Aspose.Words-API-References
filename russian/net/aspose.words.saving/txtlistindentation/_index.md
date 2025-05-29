---
title: TxtListIndentation Class
linktitle: TxtListIndentation
articleTitle: TxtListIndentation
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Saving.TxtListIndentation для настройки уровней отступа списка для бесшовного экспорта в текстовом формате. Улучшите форматирование вашего документа!
type: docs
weight: 6450
url: /ru/net/aspose.words.saving/txtlistindentation/
---
## TxtListIndentation class

Указывает, как отступают уровни списка при экспорте документа вText формат.

Чтобы узнать больше, посетите[Сохранить документ](https://docs.aspose.com/words/net/save-a-document/) документальная статья.

```csharp
public class TxtListIndentation
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [TxtListIndentation](txtlistindentation/)() | Конструктор по умолчанию. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [Character](../../aspose.words.saving/txtlistindentation/character/) { get; set; } | Возвращает или задает символ, который следует использовать для отступа уровней списка. Значение по умолчанию — '\0', что означает отсутствие отступа. |
| [Count](../../aspose.words.saving/txtlistindentation/count/) { get; set; } | Возвращает или задает количество[`Character`](./character/)использовать в качестве отступа для одного уровня списка. Значение по умолчанию — 0, что означает отсутствие отступа. |

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

* пространство имен [Aspose.Words.Saving](../../aspose.words.saving/)
* сборка [Aspose.Words](../../)
