---
title: Granularity Enum
linktitle: Granularity
articleTitle: Granularity
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.Comparing.Granularity, чтобы легко отслеживать изменения документов с точностью. Улучшите сравнение документов сегодня!
type: docs
weight: 490
url: /ru/net/aspose.words.comparing/granularity/
---
## Granularity enumeration

Указывает степень детализации изменений, которые необходимо отслеживать при сравнении двух документов.

```csharp
public enum Granularity
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| CharLevel | `0` | Указывает изменения на уровне символов. |
| WordLevel | `1` | Указывает изменения на уровне слов. |

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

* пространство имен [Aspose.Words.Comparing](../../aspose.words.comparing/)
* сборка [Aspose.Words](../../)
