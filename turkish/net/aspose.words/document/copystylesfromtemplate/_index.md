---
title: CopyStylesFromTemplate
second_title: Aspose.Words for .NET API Referansı
description: Stilleri belirtilen şablondan bir belgeye kopyalar.
type: docs
weight: 550
url: /tr/net/aspose.words/document/copystylesfromtemplate/
---
## CopyStylesFromTemplate(string) {#copystylesfromtemplate_1}

Stilleri belirtilen şablondan bir belgeye kopyalar.

```csharp
public void CopyStylesFromTemplate(string template)
```

### Notlar

Stiller bir şablondan bir belgeye kopyalandığında, belgedeki benzeri adlı stiller, şablondaki stil açıklamalarıyla eşleşecek şekilde yeniden tanımlanır. Şablondaki benzersiz stiller belgeye kopyalanır. Belgedeki benzersiz stiller olduğu gibi kalır.

### Örnekler

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

// Şablon belgesinden bir stil ile aynı ada sahip bir stil oluşturun ve onu hedef belgeye ekleyin.
style = target.Styles.Add(StyleType.Paragraph, "TemplateStyle3");
style.Font.Name = "Calibri";
style.Font.Color = Color.Orange;

Assert.AreEqual(5, target.Styles.Count);

// Tüm stilleri bir belgeden diğerine kopyalamak için yöntemi çağırmanın iki yolu vardır.
// 1 - Şablon belge nesnesini geçirme:
target.CopyStylesFromTemplate(template);

// Stilleri kopyalamak, şablon belgesindeki tüm stilleri hedefe ekler
// ve aynı ada sahip mevcut stillerin üzerine yazar.
Assert.AreEqual(7, target.Styles.Count);

Assert.AreEqual("Courier New", target.Styles["TemplateStyle3"].Font.Name);
Assert.AreEqual(Color.RoyalBlue.ToArgb(), target.Styles["TemplateStyle3"].Font.Color.ToArgb());

// 2 - Bir şablon belgesinin yerel sistem dosya adını iletme:
target.CopyStylesFromTemplate(MyDir + "Rendering.docx");

Assert.AreEqual(21, target.Styles.Count);
```

### Ayrıca bakınız

* class [Document](../)
* ad alanı [Aspose.Words](../../document/)
* toplantı [Aspose.Words](../../../)

---

## CopyStylesFromTemplate(Document) {#copystylesfromtemplate}

Stilleri belirtilen şablondan bir belgeye kopyalar.

```csharp
public void CopyStylesFromTemplate(Document template)
```

### Notlar

Stiller bir şablondan bir belgeye kopyalandığında, belgedeki benzeri adlı stiller, şablondaki stil açıklamalarıyla eşleşecek şekilde yeniden tanımlanır. Şablondaki benzersiz stiller belgeye kopyalanır. Belgedeki benzersiz stiller olduğu gibi kalır.

### Örnekler

Stillerin şablondan Belge aracılığıyla bir belgeye nasıl kopyalanacağını gösterir.

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

// Şablon belgesinden bir stil ile aynı ada sahip bir stil oluşturun ve onu hedef belgeye ekleyin.
style = target.Styles.Add(StyleType.Paragraph, "TemplateStyle3");
style.Font.Name = "Calibri";
style.Font.Color = Color.Orange;

Assert.AreEqual(5, target.Styles.Count);

// Tüm stilleri bir belgeden diğerine kopyalamak için yöntemi çağırmanın iki yolu vardır.
// 1 - Şablon belge nesnesini geçirme:
target.CopyStylesFromTemplate(template);

// Stilleri kopyalamak, şablon belgesindeki tüm stilleri hedefe ekler
// ve aynı ada sahip mevcut stillerin üzerine yazar.
Assert.AreEqual(7, target.Styles.Count);

Assert.AreEqual("Courier New", target.Styles["TemplateStyle3"].Font.Name);
Assert.AreEqual(Color.RoyalBlue.ToArgb(), target.Styles["TemplateStyle3"].Font.Color.ToArgb());

// 2 - Bir şablon belgesinin yerel sistem dosya adını iletme:
target.CopyStylesFromTemplate(MyDir + "Rendering.docx");

Assert.AreEqual(21, target.Styles.Count);
```

### Ayrıca bakınız

* class [Document](../)
* ad alanı [Aspose.Words](../../document/)
* toplantı [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
