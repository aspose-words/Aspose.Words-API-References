---
title: Document.Sections
linktitle: Sections
articleTitle: Sections
second_title: Aspose.Words для .NET
description: Изучите свойство «Разделы документа», чтобы получить доступ к полной коллекции всех разделов документа, что улучшит организацию контента и навигацию.
type: docs
weight: 390
url: /ru/net/aspose.words/document/sections/
---
## Document.Sections property

Возвращает коллекцию, представляющую все разделы документа.

```csharp
public SectionCollection Sections { get; }
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

Показывает, как указать, как новый раздел отделяется от предыдущего.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("This text is in section 1.");

// Типы разрывов разделов определяют, как новый раздел отделяется от предыдущего.
// Ниже приведены пять типов разрывов разделов.
// 1 — Начинает следующий раздел на новой странице:
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Writeln("This text is in section 2.");

Assert.AreEqual(SectionStart.NewPage, doc.Sections[1].PageSetup.SectionStart);

// 2 — Начинает следующий раздел на текущей странице:
builder.InsertBreak(BreakType.SectionBreakContinuous);
builder.Writeln("This text is in section 3.");

Assert.AreEqual(SectionStart.Continuous, doc.Sections[2].PageSetup.SectionStart);

// 3 - Начинает следующий раздел на новой четной странице:
builder.InsertBreak(BreakType.SectionBreakEvenPage);
builder.Writeln("This text is in section 4.");

Assert.AreEqual(SectionStart.EvenPage, doc.Sections[3].PageSetup.SectionStart);

// 4 — Начинает следующий раздел на новой нечетной странице:
builder.InsertBreak(BreakType.SectionBreakOddPage);
builder.Writeln("This text is in section 5.");

Assert.AreEqual(SectionStart.OddPage, doc.Sections[4].PageSetup.SectionStart);

// 5 — Начинает следующий раздел в новом столбце:
TextColumnCollection columns = builder.PageSetup.TextColumns;
columns.SetCount(2);

builder.InsertBreak(BreakType.SectionBreakNewColumn);
builder.Writeln("This text is in section 6.");

Assert.AreEqual(SectionStart.NewColumn, doc.Sections[5].PageSetup.SectionStart);

doc.Save(ArtifactsDir + "PageSetup.SetSectionStart.docx");
```

### Смотрите также

* class [SectionCollection](../../sectioncollection/)
* class [Document](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
