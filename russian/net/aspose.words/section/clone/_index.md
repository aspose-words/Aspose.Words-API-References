---
title: Section.Clone
linktitle: Clone
articleTitle: Clone
second_title: Aspose.Words для .NET
description: Легко дублируйте разделы с помощью нашего метода Section Clone. Оптимизируйте свой рабочий процесс и повысьте производительность с помощью этого мощного инструмента!
type: docs
weight: 130
url: /ru/net/aspose.words/section/clone/
---
## Section.Clone method

Создает дубликат этого раздела.

```csharp
public Section Clone()
```

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

* class [Section](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
