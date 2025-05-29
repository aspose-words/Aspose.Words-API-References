---
title: CompareOptions.Granularity
linktitle: Granularity
articleTitle: Granularity
second_title: Aspose.Words для .NET
description: Откройте для себя свойство CompareOptions Granularity, отслеживайте изменения по символам или словам для точного редактирования текста. Улучшите контроль над документами сегодня!
type: docs
weight: 40
url: /ru/net/aspose.words.comparing/compareoptions/granularity/
---
## CompareOptions.Granularity property

Указывает, отслеживаются ли изменения по символам или по словам.

```csharp
public Granularity Granularity { get; set; }
```

## Примечания

Значение по умолчанию:WordLevel .

## Примеры

Позволяет указать степень детализации при сравнении документов.

```csharp
Document docA = new Document();
DocumentBuilder builderA = new DocumentBuilder(docA);
builderA.Writeln("Alpha Lorem ipsum dolor sit amet, consectetur adipiscing elit");

Document docB = new Document();
DocumentBuilder builderB = new DocumentBuilder(docB);
builderB.Writeln("Lorems ipsum dolor sit amet consectetur - \"adipiscing\" elit");

// Укажите, отслеживаются ли изменения
// по символу ('Granularity.CharLevel') или по слову ('Granularity.WordLevel').
CompareOptions compareOptions = new CompareOptions();
compareOptions.Granularity = granularity;

docA.Compare(docB, "author", DateTime.Now, compareOptions);

// Коллекция групп ревизий первого документа содержит все различия между документами.
RevisionGroupCollection groups = docA.Revisions.Groups;
Assert.AreEqual(5, groups.Count);
```

### Смотрите также

* enum [Granularity](../../granularity/)
* class [CompareOptions](../)
* пространство имен [Aspose.Words.Comparing](../../../aspose.words.comparing/)
* сборка [Aspose.Words](../../../)
