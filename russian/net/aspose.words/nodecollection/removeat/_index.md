---
title: NodeCollection.RemoveAt
linktitle: RemoveAt
articleTitle: RemoveAt
second_title: Aspose.Words для .NET
description: Легко удаляйте узлы из вашей коллекции с помощью метода NodeCollection RemoveAt. Оптимизируйте управление документами, быстро удаляя определенные узлы.
type: docs
weight: 100
url: /ru/net/aspose.words/nodecollection/removeat/
---
## NodeCollection.RemoveAt method

Удаляет узел с указанным индексом из коллекции и из документа.

```csharp
public void RemoveAt(int index)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| index | Int32 | Индекс узла, начинающийся с нуля. Отрицательные индексы разрешены и указывают на доступ с конца списка. Например, -1 означает последний узел, -2 означает предпоследний и т. д. |

## Примеры

Показывает, как добавлять и удалять разделы в документе.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Section 1");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Section 2");

Assert.AreEqual("Section 1\x000cSection 2", doc.GetText().Trim());

// Удалить первый раздел из документа.
doc.Sections.RemoveAt(0);

Assert.AreEqual("Section 2", doc.GetText().Trim());

// Добавляем копию того, что сейчас является первым разделом, в конец документа.
int lastSectionIdx = doc.Sections.Count - 1;
Section newSection = doc.Sections[lastSectionIdx].Clone();
doc.Sections.Add(newSection);

Assert.AreEqual("Section 2\x000cSection 2", doc.GetText().Trim());
```

### Смотрите также

* class [NodeCollection](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
