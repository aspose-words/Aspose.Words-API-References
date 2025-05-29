---
title: Document.CopyStylesFromTemplate
linktitle: CopyStylesFromTemplate
articleTitle: CopyStylesFromTemplate
second_title: .NET için Aspose.Words
description: CopyStylesFromTemplate yöntemiyle seçtiğiniz şablondaki stilleri herhangi bir belgeye zahmetsizce kopyalayarak iş akışınızı ve belge tutarlılığınızı geliştirin.
type: docs
weight: 610
url: /tr/net/aspose.words/document/copystylesfromtemplate/
---
## CopyStylesFromTemplate(*string*) {#copystylesfromtemplate_1}

Belirtilen şablondan bir belgeye stilleri kopyalar.

```csharp
public void CopyStylesFromTemplate(string template)
```

## Notlar

Stiller bir şablondan bir belgeye kopyalandığında, belgedeki benzer adlı stiller şablondaki stil açıklamalarıyla eşleşecek şekilde yeniden tanımlanır. Şablondaki benzersiz stiller belgeye kopyalanır. Belgedeki benzersiz stiller bozulmadan kalır.

## Örnekler

Stillerin bir belgeden diğerine nasıl kopyalanacağını gösterir.

```csharp
// Bir belge oluşturalım ve ardından başka bir belgeye kopyalayacağımız stilleri ekleyelim.
Document template = new Document();

Style style = template.Styles.Add(StyleType.Paragraph, "TemplateStyle1");
style.Font.Name = "Times New Roman";
style.Font.Color = Color.Navy;

style = template.Styles.Add(StyleType.Paragraph, "TemplateStyle2");
style.Font.Name = "Arial";
style.Font.Color = Color.DeepSkyBlue;

style = template.Styles.Add(StyleType.Paragraph, "TemplateStyle3");
style.Font.Name = "Courier New";
style.Font.Color = Color.RoyalBlue;

Assert.AreEqual(7, template.Styles.Count);

// Stilleri kopyalayacağımız bir belge oluşturalım.
Document target = new Document();

// Şablon belgesindeki bir stille aynı adı taşıyan bir stil oluştur ve hedef belgeye ekle.
style = target.Styles.Add(StyleType.Paragraph, "TemplateStyle3");
style.Font.Name = "Calibri";
style.Font.Color = Color.Orange;

Assert.AreEqual(5, target.Styles.Count);

// Tüm stilleri bir belgeden diğerine kopyalamak için yöntemi çağırmanın iki yolu vardır.
// 1 - Şablon belge nesnesini geçirme:
target.CopyStylesFromTemplate(template);

// Stilleri kopyalamak, şablon belgesindeki tüm stilleri hedef belgeye ekler
// ve aynı adı taşıyan mevcut stilleri üzerine yazar.
Assert.AreEqual(7, target.Styles.Count);

Assert.AreEqual("Courier New", target.Styles["TemplateStyle3"].Font.Name);
Assert.AreEqual(Color.RoyalBlue.ToArgb(), target.Styles["TemplateStyle3"].Font.Color.ToArgb());

// 2 - Şablon belgesinin yerel sistem dosya adının geçirilmesi:
target.CopyStylesFromTemplate(MyDir + "Rendering.docx");

Assert.AreEqual(21, target.Styles.Count);
```

### Ayrıca bakınız

* class [Document](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)

---

## CopyStylesFromTemplate(*[Document](../)*) {#copystylesfromtemplate}

Belirtilen şablondan bir belgeye stilleri kopyalar.

```csharp
public void CopyStylesFromTemplate(Document template)
```

## Notlar

Stiller bir şablondan bir belgeye kopyalandığında, belgedeki benzer adlı stiller şablondaki stil açıklamalarıyla eşleşecek şekilde yeniden tanımlanır. Şablondaki benzersiz stiller belgeye kopyalanır. Belgedeki benzersiz stiller bozulmadan kalır.

## Örnekler

Şablondan belgeye Document aracılığıyla stillerin nasıl kopyalanacağını gösterir.

```csharp
Document template = new Document(MyDir + "Rendering.docx");
Document target = new Document(MyDir + "Document.docx");

target.CopyStylesFromTemplate(template);
```

Stillerin bir belgeden diğerine nasıl kopyalanacağını gösterir.

```csharp
// Bir belge oluşturalım ve ardından başka bir belgeye kopyalayacağımız stilleri ekleyelim.
Document template = new Document();

Style style = template.Styles.Add(StyleType.Paragraph, "TemplateStyle1");
style.Font.Name = "Times New Roman";
style.Font.Color = Color.Navy;

style = template.Styles.Add(StyleType.Paragraph, "TemplateStyle2");
style.Font.Name = "Arial";
style.Font.Color = Color.DeepSkyBlue;

style = template.Styles.Add(StyleType.Paragraph, "TemplateStyle3");
style.Font.Name = "Courier New";
style.Font.Color = Color.RoyalBlue;

Assert.AreEqual(7, template.Styles.Count);

// Stilleri kopyalayacağımız bir belge oluşturalım.
Document target = new Document();

// Şablon belgesindeki bir stille aynı adı taşıyan bir stil oluştur ve hedef belgeye ekle.
style = target.Styles.Add(StyleType.Paragraph, "TemplateStyle3");
style.Font.Name = "Calibri";
style.Font.Color = Color.Orange;

Assert.AreEqual(5, target.Styles.Count);

// Tüm stilleri bir belgeden diğerine kopyalamak için yöntemi çağırmanın iki yolu vardır.
// 1 - Şablon belge nesnesini geçirme:
target.CopyStylesFromTemplate(template);

// Stilleri kopyalamak, şablon belgesindeki tüm stilleri hedef belgeye ekler
// ve aynı adı taşıyan mevcut stilleri üzerine yazar.
Assert.AreEqual(7, target.Styles.Count);

Assert.AreEqual("Courier New", target.Styles["TemplateStyle3"].Font.Name);
Assert.AreEqual(Color.RoyalBlue.ToArgb(), target.Styles["TemplateStyle3"].Font.Color.ToArgb());

// 2 - Şablon belgesinin yerel sistem dosya adının geçirilmesi:
target.CopyStylesFromTemplate(MyDir + "Rendering.docx");

Assert.AreEqual(21, target.Styles.Count);
```

### Ayrıca bakınız

* class [Document](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
