---
title: PageSetup.SuppressEndnotes
linktitle: SuppressEndnotes
articleTitle: SuppressEndnotes
second_title: Aspose.Words для .NET
description: Узнайте, как свойство PageSetup SuppressEndnotes улучшает макет документа, управляя размещением концевых сносок для более понятных и организованных разделов.
type: docs
weight: 410
url: /ru/net/aspose.words/pagesetup/suppressendnotes/
---
## PageSetup.SuppressEndnotes property

Истинно, если концевые сноски печатаются в конце следующего раздела, который не подавляет концевые сноски. Подавленные концевые сноски печатаются перед концевыми сносками в этом разделе.

```csharp
public bool SuppressEndnotes { get; set; }
```

## Примеры

Показывает, как сохранять концевые сноски в конце каждого раздела и изменять их положение.

```csharp
public void SuppressEndnotes()
{
    Document doc = new Document();
    doc.RemoveAllChildren();

     // По умолчанию документ компилирует все концевые сноски в конце.
    Assert.AreEqual(EndnotePosition.EndOfDocument, doc.EndnoteOptions.Position);

    // Мы используем свойство "Position" объекта "EndnoteOptions" документа
     // вместо этого собирать концевые сноски в конце каждого раздела.
    doc.EndnoteOptions.Position = EndnotePosition.EndOfSection;

    InsertSectionWithEndnote(doc, "Section 1", "Endnote 1, will stay in section 1");
    InsertSectionWithEndnote(doc, "Section 2", "Endnote 2, will be pushed down to section 3");
    InsertSectionWithEndnote(doc, "Section 3", "Endnote 3, will stay in section 3");

    // При отображении соответствующих концевых сносок в разделах мы можем установить флаг «SuppressEndnotes»
    // объекта "PageSetup" раздела на "true", чтобы вернуться к поведению по умолчанию и передать его концевые сноски
    // к следующему разделу.
    PageSetup pageSetup = doc.Sections[1].PageSetup;
    pageSetup.SuppressEndnotes = true;

    doc.Save(ArtifactsDir + "PageSetup.SuppressEndnotes.docx");
}

/// <summary>
/// Добавить раздел с текстом и концевой сноской к документу.
/// </summary>
private static void InsertSectionWithEndnote(Document doc, string sectionBodyText, string endnoteText)
{
    Section section = new Section(doc);

    doc.AppendChild(section);

    Body body = new Body(doc);
    section.AppendChild(body);

    Assert.AreEqual(section, body.ParentNode);

    Paragraph para = new Paragraph(doc);
    body.AppendChild(para);

    Assert.AreEqual(body, para.ParentNode);

    DocumentBuilder builder = new DocumentBuilder(doc);
    builder.MoveTo(para);
    builder.Write(sectionBodyText);
    builder.InsertFootnote(FootnoteType.Endnote, endnoteText);
}
```

### Смотрите также

* class [PageSetup](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
