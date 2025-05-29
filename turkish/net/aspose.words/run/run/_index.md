---
title: Run
linktitle: Run
articleTitle: Run
second_title: .NET için Aspose.Words
description: Run sınıfı örneğinizi zahmetsizce oluşturun ve özelleştirin. Akıcı performans ve gelişmiş işlevsellik için güçlü özelliklerin kilidini açın.
type: docs
weight: 10
url: /tr/net/aspose.words/run/run/
---
## Run(*[DocumentBase](../../documentbase/)*) {#constructor}

Yeni bir örneğini başlatır[`Run`](../) sınıf.

```csharp
public Run(DocumentBase doc)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| doc | DocumentBase | Sahip belgesi. |

## Notlar

Ne zaman[`Run`](../) oluşturulduğunda, belirtilen belgeye aittir, ancak henüz belgenin bir parçası değildir ve[`ParentNode`](../../node/parentnode/) dır`hükümsüz`.

Eklemek için[`Run`](../) belge kullanımına[`InsertAfter`](../../compositenode/insertafter/) veya[`InsertBefore`](../../compositenode/insertbefore/) Çalıştırmanın eklenmesini istediğiniz paragrafta yazın.

## Örnekler

Aspose.Words belgesinin elle nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();

// Boş bir belge bir bölüm, bir gövde ve bir paragraftan oluşur.
// Tüm bu düğümleri kaldırmak için "RemoveAllChildren" yöntemini çağırın,
// ve çocuğu olmayan bir belge düğümüyle sonuçlanır.
doc.RemoveAllChildren();

// Bu belgenin artık içerik ekleyebileceğimiz bileşik alt düğümleri yok.
// Düzenlemek istersek, düğüm koleksiyonunu yeniden doldurmamız gerekecektir.
// İlk önce yeni bir bölüm oluşturun ve ardından onu kök belge düğümüne bir alt bölüm olarak ekleyin.
Section section = new Section(doc);
doc.AppendChild(section);

// Bölüm için bazı sayfa düzeni özelliklerini ayarlayın.
section.PageSetup.SectionStart = SectionStart.NewPage;
section.PageSetup.PaperSize = PaperSize.Letter;

// Bir bölümün, tüm içeriklerini barındıracak ve görüntüleyecek bir gövdeye ihtiyacı vardır
// bölümün üstbilgisi ve altbilgisi arasındaki sayfada.
Body body = new Body(doc);
section.AppendChild(body);

// Bir paragraf oluştur, bazı biçimlendirme özelliklerini ayarla ve sonra onu gövdeye bir alt paragraf olarak ekle.
Paragraph para = new Paragraph(doc);

para.ParagraphFormat.StyleName = "Heading 1";
para.ParagraphFormat.Alignment = ParagraphAlignment.Center;

body.AppendChild(para);

// Son olarak, belgeyi yapmak için biraz içerik ekleyin. Bir çalışma oluşturun,
// Görünümünü ve içeriğini ayarlayın ve ardından paragrafın bir alt öğesi olarak ekleyin.
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

Yeni bir örneğini başlatır**Koşmak** sınıf.

```csharp
public Run(DocumentBase doc, string text)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| doc | DocumentBase | Sahip belgesi. |
| text | String | Koşunun metni. |

## Notlar

Ne zaman[`Run`](../) oluşturulduğunda, belirtilen belgeye aittir, ancak henüz belgenin bir parçası değildir ve[`ParentNode`](../../node/parentnode/) dır`hükümsüz`.

Eklemek için[`Run`](../) belge kullanımına[`InsertAfter`](../../compositenode/insertafter/) veya[`InsertBefore`](../../compositenode/insertbefore/) Çalıştırmanın eklenmesini istediğiniz paragrafta yazın.

## Örnekler

Bir metin dizisinin font özelliğini kullanarak nasıl biçimlendirileceğini gösterir.

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
