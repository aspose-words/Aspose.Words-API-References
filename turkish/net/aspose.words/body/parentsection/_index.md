---
title: Body.ParentSection
linktitle: ParentSection
articleTitle: ParentSection
second_title: .NET için Aspose.Words
description: Bir hikayenin ana bölümüne kolayca erişmek ve içerik yönetimi verimliliğinizi artırmak için Body ParentSection özelliğini keşfedin.
type: docs
weight: 30
url: /tr/net/aspose.words/body/parentsection/
---
## Body.ParentSection property

Bu hikayenin üst bölümünü alır.

```csharp
public Section ParentSection { get; }
```

## Notlar

`ParentSection` eşdeğerdir[`ParentNode`](../../node/parentnode/) atıldı[`Section`](../../section/).

## Örnekler

Her bölümün sonunda dipnotların nasıl saklanacağını ve konumlarının nasıl değiştirileceğini gösterir.

```csharp
public void SuppressEndnotes()
{
    Document doc = new Document();
    doc.RemoveAllChildren();

     // Varsayılan olarak, bir belgenin sonunda tüm dipnotlar derlenir.
    Assert.AreEqual(EndnotePosition.EndOfDocument, doc.EndnoteOptions.Position);

    // Belgenin "EndnoteOptions" nesnesinin "Position" özelliğini kullanıyoruz
     // bunun yerine her bölümün sonunda dipnotları toplamak.
    doc.EndnoteOptions.Position = EndnotePosition.EndOfSection;

    InsertSectionWithEndnote(doc, "Section 1", "Endnote 1, will stay in section 1");
    InsertSectionWithEndnote(doc, "Section 2", "Endnote 2, will be pushed down to section 3");
    InsertSectionWithEndnote(doc, "Section 3", "Endnote 3, will stay in section 3");

    // Bölümlerin kendi dipnotlarını görüntülemesini sağlarken "SuppressEndnotes" bayrağını ayarlayabiliriz
    // bir bölümün "PageSetup" nesnesinin varsayılan davranışa geri dönmesi ve dipnotlarını geçirmesi için "true" olarak ayarlanması
    // bir sonraki bölüme.
    PageSetup pageSetup = doc.Sections[1].PageSetup;
    pageSetup.SuppressEndnotes = true;

    doc.Save(ArtifactsDir + "PageSetup.SuppressEndnotes.docx");
}

/// <summary>
/// Bir belgeye metin ve son not içeren bir bölüm ekleyin.
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

### Ayrıca bakınız

* class [Section](../../section/)
* class [Body](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
