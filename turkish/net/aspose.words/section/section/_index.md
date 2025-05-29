---
title: Section
linktitle: Section
articleTitle: Section
second_title: .NET için Aspose.Words
description: Section Constructor'ımızla dinamik web bölümlerini zahmetsizce oluşturun. En iyi site performansı için Section sınıfınızı kolayca başlatın ve özelleştirin.
type: docs
weight: 10
url: /tr/net/aspose.words/section/section/
---
## Section constructor

Section sınıfının yeni bir örneğini başlatır.

```csharp
public Section(DocumentBase doc)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| doc | DocumentBase | Sahip belgesi. |

## Notlar

Bölüm oluşturulduğunda belirtilen belgeye aittir, ancak henüz belgenin bir parçası değildir ve[`ParentNode`](../../node/parentnode/) dır`hükümsüz`.

Dahil etmek için[`Section`](../) bir belgeye kullanım[`InsertAfter`](../../compositenode/insertafter/) ve [`InsertBefore`](../../compositenode/insertbefore/) yöntemleri[`Document`](../../document/) VEYA [`Add`](../../nodecollection/add/) Ve[`Insert`](../../nodecollection/insert/) yöntemleri[`Sections`](../../document/sections/) mülk.

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
* class [Section](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
