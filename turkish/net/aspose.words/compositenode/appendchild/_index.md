---
title: CompositeNode.AppendChild
linktitle: AppendChild
articleTitle: AppendChild
second_title: Aspose.Words for .NET
description: CompositeNode AppendChild yöntem. Belirtilen düğümü bu düğüm için alt düğümler listesinin sonuna ekler C#'da.
type: docs
weight: 60
url: /tr/net/aspose.words/compositenode/appendchild/
---
## CompositeNode.AppendChild method

Belirtilen düğümü, bu düğüm için alt düğümler listesinin sonuna ekler.

```csharp
public Node AppendChild(Node newChild)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| newChild | Node | Eklenecek düğüm. |

### Geri dönüş değeri

Düğüm eklendi.

## Notlar

Eğer*newChild* zaten ağaçtaysa, önce kaldırılır.

Eklenen düğüm başka bir belgeden oluşturulmuşsa kullanmalısınız[`ImportNode`](../../documentbase/importnode/) Düğümü geçerli belgeye aktarmak için. İçe aktarılan düğüm daha sonra geçerli belgeye eklenebilir.

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

* class [Node](../../node/)
* class [CompositeNode](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
