---
title: CompositeNode.AppendChild
linktitle: AppendChild
articleTitle: AppendChild
second_title: .NET için Aspose.Words
description: CompositeNode AppendChild yönteminin, düğümleri alt düğüm listenize sorunsuz bir şekilde ekleyerek kodlamanızı nasıl geliştirdiğini keşfedin. Geliştirme verimliliğinizi artırın!
type: docs
weight: 80
url: /tr/net/aspose.words/compositenode/appendchild/
---
## CompositeNode.AppendChild&lt;T&gt; method

Belirtilen düğümü bu düğüm için alt düğümler listesinin sonuna ekler.

```csharp
public T AppendChild<T>(T newChild)
    where T : Node
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| newChild | T | Eklenecek düğüm. |

### Geri dönüş değeri

Düğüm eklendi.

## Notlar

Eğer*newChild* Ağaçta zaten varsa, önce o kaldırılır.

Eklenen düğüm başka bir belgeden oluşturulduysa, kullanmalısınız[`ImportNode`](../../documentbase/importnode/) Düğümü geçerli belgeye aktarmak için. Daha sonra içe aktarılan düğüm geçerli belgeye eklenebilir.

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

* class [Node](../../node/)
* class [CompositeNode](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
