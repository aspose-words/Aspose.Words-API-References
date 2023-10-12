---
title: Body.ParentSection
second_title: Справочник по API Aspose.Words для .NET
description: Body свойство. Получает родительский раздел этой статьи.
type: docs
weight: 30
url: /ru/net/aspose.words/body/parentsection/
---
## Body.ParentSection property

Получает родительский раздел этой статьи.

```csharp
public Section ParentSection { get; }
```

### Примечания

`ParentSection` эквивалентно[`ParentNode`](../../node/parentnode/) брошен в[`Section`](../../section/).

### Примеры

Показывает, как сохранять концевые сноски в конце каждого раздела и изменять их положение.

```csharp
public void SuppressEndnotes()
{
    Document doc = new Document();
    doc.RemoveAllChildren();

     // По умолчанию документ компилирует все концевые сноски в конце.
    Assert.AreEqual(EndnotePosition.EndOfDocument, doc.EndnoteOptions.Position);

    // Мы используем свойство «Позиция» объекта «EndnoteOptions» документа.
     // вместо этого собирать сноски в конце каждого раздела.
    doc.EndnoteOptions.Position = EndnotePosition.EndOfSection;

    InsertSectionWithEndnote(doc, "Section 1", "Endnote 1, will stay in section 1");
    InsertSectionWithEndnote(doc, "Section 2", "Endnote 2, will be pushed down to section 3");
    InsertSectionWithEndnote(doc, "Section 3", "Endnote 3, will stay in section 3");

    // При получении разделов для отображения соответствующих концевых сносок мы можем установить флаг «SuppressEndnotes»
    // объекта «PageSetup» раздела на «true», чтобы вернуться к поведению по умолчанию и передать его концевые сноски
    // переходим к следующему разделу.
    PageSetup pageSetup = doc.Sections[1].PageSetup;
    pageSetup.SuppressEndnotes = true;

    doc.Save(ArtifactsDir + "PageSetup.SuppressEndnotes.docx");
}

/// <summary>
/// Добавляем в документ раздел с текстом и сноской.
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
* пространство имен [Aspose.Words](../../body/)
* сборка [Aspose.Words](../../../)


