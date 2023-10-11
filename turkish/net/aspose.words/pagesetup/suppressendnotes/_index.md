---
title: PageSetup.SuppressEndnotes
second_title: Aspose.Words for .NET API Referansı
description: PageSetup mülk. Son notlar son notları gizlemeyen bir sonraki bölümün sonunda yazdırılıyorsa doğrudur. Bastırılmış son notlar o bölümdeki son notlardan önce yazdırılır.
type: docs
weight: 410
url: /tr/net/aspose.words/pagesetup/suppressendnotes/
---
## PageSetup.SuppressEndnotes property

Son notlar, son notları gizlemeyen bir sonraki bölümün sonunda yazdırılıyorsa doğrudur. Bastırılmış son notlar, o bölümdeki son notlardan önce yazdırılır.

```csharp
public bool SuppressEndnotes { get; set; }
```

### Örnekler

Her bölümün sonunda son notların nasıl saklanacağını ve konumlarının nasıl değiştirileceğini gösterir.

```csharp
public void SuppressEndnotes()
{
    Document doc = new Document();
    doc.RemoveAllChildren();

     // Varsayılan olarak bir belge tüm son notları sonunda derler.
    Assert.AreEqual(EndnotePosition.EndOfDocument, doc.EndnoteOptions.Position);

    // Belgenin "EndnoteOptions" nesnesinin "Position" özelliğini kullanıyoruz
     // bunun yerine her bölümün sonundaki son notları toplamak için.
    doc.EndnoteOptions.Position = EndnotePosition.EndOfSection;

    InsertSectionWithEndnote(doc, "Section 1", "Endnote 1, will stay in section 1");
    InsertSectionWithEndnote(doc, "Section 2", "Endnote 2, will be pushed down to section 3");
    InsertSectionWithEndnote(doc, "Section 3", "Endnote 3, will stay in section 3");

    // İlgili son notlarını gösterecek bölümleri alırken, "Endnotes'ı Bastır" bayrağını ayarlayabiliriz
    // varsayılan davranışa geri dönmek ve son notlarını iletmek için bir bölümün "PageSetup" nesnesini "true" olarak ayarlayın
    //sonraki bölüme geçiyoruz.
    PageSetup pageSetup = doc.Sections[1].PageSetup;
    pageSetup.SuppressEndnotes = true;

    doc.Save(ArtifactsDir + "PageSetup.SuppressEndnotes.docx");
}

/// <summary>
/// Belgeye metin içeren bir bölüm ve son not ekleyin.
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
* ad alanı [Aspose.Words](../../pagesetup/)
* toplantı [Aspose.Words](../../../)


