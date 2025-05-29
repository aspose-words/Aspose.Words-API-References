---
title: Section.HeadersFooters
linktitle: HeadersFooters
articleTitle: HeadersFooters
second_title: Aspose.Words для .NET
description: Легко получайте доступ и управляйте заголовками и колонтитулами разделов с помощью нашей интуитивно понятной функции свойств. Улучшите организацию и представление документов сегодня!
type: docs
weight: 30
url: /ru/net/aspose.words/section/headersfooters/
---
## Section.HeadersFooters property

Предоставляет доступ к узлам верхних и нижних колонтитулов раздела.

```csharp
public HeaderFooterCollection HeadersFooters { get; }
```

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

Показывает, как удалить все нижние колонтитулы из документа.

```csharp
Document doc = new Document(MyDir + "Header and footer types.docx");

// Проходим по каждому разделу и удаляем нижние колонтитулы всех видов.
foreach (Section section in doc.OfType<Section>())
{
    // Существует три типа нижних и верхних колонтитулов.
    // 1 — «Первый» верхний/нижний колонтитул, который отображается только на первой странице раздела.
    HeaderFooter footer = section.HeadersFooters[HeaderFooterType.FooterFirst];
    footer?.Remove();

    // 2 — «Основной» верхний/нижний колонтитул, который отображается на нечетных страницах.
    footer = section.HeadersFooters[HeaderFooterType.FooterPrimary];
    footer?.Remove();

     // 3 - «Четный» верхний/нижний колонтитул, который отображается на четных страницах.
    footer = section.HeadersFooters[HeaderFooterType.FooterEven];
    footer?.Remove();

    Assert.AreEqual(0, section.HeadersFooters.Count(hf => !((HeaderFooter)hf).IsHeader));
}

doc.Save(ArtifactsDir + "HeaderFooter.RemoveFooters.docx");
```

### Смотрите также

* class [HeaderFooterCollection](../../headerfootercollection/)
* class [Section](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
