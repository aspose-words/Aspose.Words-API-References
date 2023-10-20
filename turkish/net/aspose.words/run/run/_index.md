---
title: Run
linktitle: Run
articleTitle: Run
second_title: Aspose.Words for .NET
description: Run inşaatçı. Yeni bir örneğini başlatırRun class C#'da.
type: docs
weight: 10
url: /tr/net/aspose.words/run/run/
---
## Run(*[DocumentBase](../../documentbase/)*) {#constructor}

Yeni bir örneğini başlatır[`Run`](../) class.

```csharp
public Run(DocumentBase doc)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| doc | DocumentBase | Sahibi belgesi. |

## Notlar

Ne zaman[`Run`](../) oluşturulduysa, belirtilen belgeye aittir ancak henüz değildir ve belgenin bir parçası değildir ve[`ParentNode`](../../node/parentnode/) dır-dir`hükümsüz`.

Eklemek[`Run`](../) belge kullanımına[`InsertAfter`](../../compositenode/insertafter/) veya[`InsertBefore`](../../compositenode/insertbefore/) Çalıştırmanın eklenmesini istediğiniz paragrafta .

## Örnekler

Aspose.Words belgesinin elle nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();

// Boş bir belge bir bölüm, bir gövde ve bir paragraftan oluşur.
// Tüm bu düğümleri kaldırmak için "RemoveAllChildren" yöntemini çağırın,
// ve çocuğu olmayan bir belge düğümü elde ederiz.
doc.RemoveAllChildren();

// Bu belgede artık içerik ekleyebileceğimiz bileşik alt düğüm yok.
// Eğer onu düzenlemek istiyorsak, düğüm koleksiyonunu yeniden doldurmamız gerekecek.
// Öncelikle yeni bir bölüm oluşturun ve ardından bunu alt öğe olarak kök belge düğümüne ekleyin.
Section section = new Section(doc);
doc.AppendChild(section);

// Bölüm için bazı sayfa yapısı özelliklerini ayarlayın.
section.PageSetup.SectionStart = SectionStart.NewPage;
section.PageSetup.PaperSize = PaperSize.Letter;

// Bir bölümün tüm içeriğini içerecek ve görüntüleyecek bir gövdeye ihtiyacı vardır
// bölümün üstbilgisi ve altbilgisi arasındaki sayfada.
Body body = new Body(doc);
section.AppendChild(body);

// Bir paragraf oluşturun, bazı biçimlendirme özelliklerini ayarlayın ve ardından onu alt öğe olarak gövdeye ekleyin.
Paragraph para = new Paragraph(doc);

para.ParagraphFormat.StyleName = "Heading 1";
para.ParagraphFormat.Alignment = ParagraphAlignment.Center;

body.AppendChild(para);

// Son olarak belgeyi yapmak için biraz içerik ekleyin. Bir koşu oluşturun,
// görünüşünü ve içeriğini ayarlayın ve ardından onu alt öğe olarak paragrafa ekleyin.
Run run = new Run(doc);
run.Text = "Hello World!";
run.Font.Color = Color.Red;
para.AppendChild(run);

Assert.AreEqual("Hello World!", doc.GetText().Trim());

doc.Save(ArtifactsDir + "Section.CreateManually.docx");
```

### Ayrıca bakınız

* class [DocumentBase](../../documentbase/)
* class [Run](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)

---

## Run(*[DocumentBase](../../documentbase/), string*) {#constructor_1}

Yeni bir örneğini başlatır**Koşmak** class.

```csharp
public Run(DocumentBase doc, string text)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| doc | DocumentBase | Sahibi belgesi. |
| text | String | Çalıştırmanın metni. |

## Notlar

Ne zaman[`Run`](../) oluşturulduysa, belirtilen belgeye aittir ancak henüz değildir ve belgenin bir parçası değildir ve[`ParentNode`](../../node/parentnode/) dır-dir`hükümsüz`.

Eklemek[`Run`](../) belge kullanımına[`InsertAfter`](../../compositenode/insertafter/) veya[`InsertBefore`](../../compositenode/insertbefore/) Çalıştırmanın eklenmesini istediğiniz paragrafta .

## Örnekler

Font özelliğini kullanarak bir metin dizisinin nasıl biçimlendirileceğini gösterir.

```csharp
Document doc = new Document();
Run run = new Run(doc, "Hello world!");

Aspose.Words.Font font = run.Font;
font.Name = "Courier New";
font.Size = 36;
font.HighlightColor = Color.Yellow;

doc.FirstSection.Body.FirstParagraph.AppendChild(run);
doc.Save(ArtifactsDir + "Font.CreateFormattedRun.docx");
```

### Ayrıca bakınız

* class [DocumentBase](../../documentbase/)
* class [Run](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
