---
title: PageSetup.SuppressEndnotes
linktitle: SuppressEndnotes
articleTitle: SuppressEndnotes
second_title: .NET için Aspose.Words
description: PageSetup SuppressEndnotes özelliğinin, daha net ve düzenli bölümler için son not yerleşimini kontrol ederek belge düzeninizi nasıl geliştirdiğini keşfedin.
type: docs
weight: 410
url: /tr/net/aspose.words/pagesetup/suppressendnotes/
---
## PageSetup.SuppressEndnotes property

Son notlar, son notları bastırmayan bir sonraki bölümün sonunda yazdırılırsa doğrudur. Bastırılmış son notlar, o bölümdeki son notlardan önce yazdırılır.

```csharp
public bool SuppressEndnotes { get; set; }
```

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

* class [PageSetup](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
