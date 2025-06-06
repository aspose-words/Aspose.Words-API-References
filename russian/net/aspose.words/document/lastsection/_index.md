---
title: Document.LastSection
linktitle: LastSection
articleTitle: LastSection
second_title: Aspose.Words для .NET
description: Откройте для себя свойство LastSection, которое позволяет легко получить доступ к последнему разделу документа, повышая эффективность навигации и управления контентом.
type: docs
weight: 250
url: /ru/net/aspose.words/document/lastsection/
---
## Document.LastSection property

Получает последний раздел в документе.

```csharp
public Section LastSection { get; }
```

## Примечания

Возврат`нулевой`если нет разделов.

## Примеры

Показывает, как создать новый раздел с помощью конструктора документов.

```csharp
Document doc = new Document();

// Пустой документ по умолчанию содержит один раздел,
// который содержит дочерние узлы, которые мы можем редактировать.
Assert.AreEqual(1, doc.Sections.Count);

// Используйте конструктор документов, чтобы добавить текст в первый раздел.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Создайте второй раздел, вставив разрыв раздела.
builder.InsertBreak(BreakType.SectionBreakNewPage);

Assert.AreEqual(2, doc.Sections.Count);

// Каждый раздел имеет свои собственные настройки страницы.
// Мы можем разделить текст во втором разделе на два столбца.
// Это не повлияет на текст в первом разделе.
doc.LastSection.PageSetup.TextColumns.SetCount(2);
builder.Writeln("Column 1.");
builder.InsertBreak(BreakType.ColumnBreak);
builder.Writeln("Column 2.");

Assert.AreEqual(1, doc.FirstSection.PageSetup.TextColumns.Count);
Assert.AreEqual(2, doc.LastSection.PageSetup.TextColumns.Count);

doc.Save(ArtifactsDir + "Section.Create.docx");
```

### Смотрите также

* class [Section](../../section/)
* class [Document](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
