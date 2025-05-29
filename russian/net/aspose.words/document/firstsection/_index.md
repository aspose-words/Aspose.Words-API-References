---
title: Document.FirstSection
linktitle: FirstSection
articleTitle: FirstSection
second_title: Aspose.Words для .NET
description: Получите первый раздел вашего документа без усилий. Улучшите свой рабочий процесс с помощью нашего свойства Document FirstSection для упрощенной организации.
type: docs
weight: 140
url: /ru/net/aspose.words/document/firstsection/
---
## Document.FirstSection property

Получает первый раздел в документе.

```csharp
public Section FirstSection { get; }
```

## Примечания

Возврат`нулевой`если нет разделов.

## Примеры

Показывает, как заменить текст в нижнем колонтитуле документа.

```csharp
Document doc = new Document(MyDir + "Footer.docx");

HeaderFooterCollection headersFooters = doc.FirstSection.HeadersFooters;
HeaderFooter footer = headersFooters[HeaderFooterType.FooterPrimary];

FindReplaceOptions options = new FindReplaceOptions
{
    MatchCase = false,
    FindWholeWordsOnly = false
};

int currentYear = DateTime.Now.Year;
footer.Range.Replace("(C) 2006 Aspose Pty Ltd.", $"Copyright (C) {currentYear} by Aspose Pty Ltd.", options);

doc.Save(ArtifactsDir + "HeaderFooter.ReplaceText.docx");
```

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

Показывает, как перебирать дочерние элементы составного узла.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Section 1");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("Primary header");
builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.Write("Primary footer");

Section section = doc.FirstSection;

// Раздел — это составной узел, который может содержать дочерние узлы,
// но только если эти дочерние узлы имеют тип узла "Body" или "HeaderFooter".
foreach (Node node in section)
{
    switch (node.NodeType)
    {
        case NodeType.Body:
        {
            Body body = (Body)node;

            Console.WriteLine("Body:");
            Console.WriteLine($"\t\"{body.GetText().Trim()}\"");
            break;
        }
        case NodeType.HeaderFooter:
        {
            HeaderFooter headerFooter = (HeaderFooter)node;

            Console.WriteLine($"HeaderFooter type: {headerFooter.HeaderFooterType}:");
            Console.WriteLine($"\t\"{headerFooter.GetText().Trim()}\"");
            break;
        }
        default:
        {
            throw new Exception("Unexpected node type in a section.");
        }
    }
}
```

### Смотрите также

* class [Section](../../section/)
* class [Document](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
