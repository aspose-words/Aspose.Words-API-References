---
title: Document.CopyStylesFromTemplate
linktitle: CopyStylesFromTemplate
articleTitle: CopyStylesFromTemplate
second_title: Aspose.Words for .NET
description: Document CopyStylesFromTemplate yöntem. Stilleri belirtilen şablondan bir belgeye kopyalar C#'da.
type: docs
weight: 570
url: /tr/net/aspose.words/document/copystylesfromtemplate/
---
## CopyStylesFromTemplate(*string*) {#copystylesfromtemplate_1}

Stilleri belirtilen şablondan bir belgeye kopyalar.

```csharp
public void CopyStylesFromTemplate(string template)
```

## Notlar

Stiller bir şablondan bir belgeye kopyalandığında, belgedeki benzer isimli stiller, şablondaki stil açıklamalarıyla eşleşecek şekilde yeniden tanımlanır. Şablondaki benzersiz stiller belgeye kopyalanır. Belgedeki benzersiz stiller bozulmadan kalır.

## Örnekler

Stillerin bir belgeden diğerine nasıl kopyalanacağını gösterir.

```csharp
// Bir belge oluşturun ve ardından başka bir belgeye kopyalayacağımız stilleri ekleyin.
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

// Stilleri kopyalayacağımız bir belge oluşturun.
Document target = new Document();

// Şablon belgesindeki stille aynı adı taşıyan bir stil oluşturun ve bunu hedef belgeye ekleyin.
style = target.Styles.Add(StyleType.Paragraph, "TemplateStyle3");
style.Font.Name = "Calibri";
style.Font.Color = Color.Orange;

Assert.AreEqual(5, target.Styles.Count);

// Tüm stilleri bir belgeden diğerine kopyalama yöntemini çağırmanın iki yolu vardır.
// 1 - Şablon belge nesnesinin iletilmesi:
target.CopyStylesFromTemplate(template);

// Stillerin kopyalanması şablon belgesindeki tüm stilleri hedefe ekler
// ve aynı adı taşıyan mevcut stillerin üzerine yazar.
Assert.AreEqual(7, target.Styles.Count);

Assert.AreEqual("Courier New", target.Styles["TemplateStyle3"].Font.Name);
Assert.AreEqual(Color.RoyalBlue.ToArgb(), target.Styles["TemplateStyle3"].Font.Color.ToArgb());

// 2 - Bir şablon belgesinin yerel sistem dosya adının iletilmesi:
target.CopyStylesFromTemplate(MyDir + "Rendering.docx");

Assert.AreEqual(21, target.Styles.Count);
```

### Ayrıca bakınız

* class [Document](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)

---

## CopyStylesFromTemplate(*[Document](../)*) {#copystylesfromtemplate}

Stilleri belirtilen şablondan bir belgeye kopyalar.

```csharp
public void CopyStylesFromTemplate(Document template)
```

## Notlar

Stiller bir şablondan bir belgeye kopyalandığında, belgedeki benzer isimli stiller, şablondaki stil açıklamalarıyla eşleşecek şekilde yeniden tanımlanır. Şablondaki benzersiz stiller belgeye kopyalanır. Belgedeki benzersiz stiller bozulmadan kalır.

## Örnekler

Stillerin şablondan belgeye Belge aracılığıyla nasıl kopyalanacağını gösterir.

```csharp
Document template = new Document(MyDir + "Rendering.docx");
Document target = new Document(MyDir + "Document.docx");

target.CopyStylesFromTemplate(template);
```

Stillerin bir belgeden diğerine nasıl kopyalanacağını gösterir.

```csharp
// Bir belge oluşturun ve ardından başka bir belgeye kopyalayacağımız stilleri ekleyin.
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

// Stilleri kopyalayacağımız bir belge oluşturun.
Document target = new Document();

// Şablon belgesindeki stille aynı adı taşıyan bir stil oluşturun ve bunu hedef belgeye ekleyin.
style = target.Styles.Add(StyleType.Paragraph, "TemplateStyle3");
style.Font.Name = "Calibri";
style.Font.Color = Color.Orange;

Assert.AreEqual(5, target.Styles.Count);

// Tüm stilleri bir belgeden diğerine kopyalama yöntemini çağırmanın iki yolu vardır.
// 1 - Şablon belge nesnesinin iletilmesi:
target.CopyStylesFromTemplate(template);

// Stillerin kopyalanması şablon belgesindeki tüm stilleri hedefe ekler
// ve aynı adı taşıyan mevcut stillerin üzerine yazar.
Assert.AreEqual(7, target.Styles.Count);

Assert.AreEqual("Courier New", target.Styles["TemplateStyle3"].Font.Name);
Assert.AreEqual(Color.RoyalBlue.ToArgb(), target.Styles["TemplateStyle3"].Font.Color.ToArgb());

// 2 - Bir şablon belgesinin yerel sistem dosya adının iletilmesi:
target.CopyStylesFromTemplate(MyDir + "Rendering.docx");

Assert.AreEqual(21, target.Styles.Count);
```

### Ayrıca bakınız

* class [Document](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
