---
title: Body.ParentSection
linktitle: ParentSection
articleTitle: ParentSection
second_title: Aspose.Words для .NET
description: Откройте для себя свойство Body ParentSection, чтобы легко получить доступ к родительскому разделу истории и повысить эффективность управления контентом.
type: docs
weight: 30
url: /ru/net/aspose.words/body/parentsection/
---
## Body.ParentSection property

Получает родительский раздел этой истории.

```csharp
public Section ParentSection { get; }
```

## Примечания

`ParentSection` эквивалентно[`ParentNode`](../../node/parentnode/) отлитый в[`Section`](../../section/).

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

* class [Section](../../section/)
* class [Body](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
