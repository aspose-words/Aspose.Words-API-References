---
title: Document.AutomaticallyUpdateStyles
second_title: Aspose.Words for .NET API Referansı
description: Document mülk. Belgedeki stillerin belge MS Wordde her açıldığında ekli şablondaki stilleriyle eşleşecek şekilde güncellenip güncellenmediğini belirten bir bayrak alır veya ayarlar.
type: docs
weight: 30
url: /tr/net/aspose.words/document/automaticallyupdatestyles/
---
## Document.AutomaticallyUpdateStyles property

Belgedeki stillerin, belge MS Word'de her açıldığında ekli şablondaki stilleriyle eşleşecek şekilde güncellenip güncellenmediğini belirten bir bayrak alır veya ayarlar.

```csharp
public bool AutomaticallyUpdateStyles { get; set; }
```

### Örnekler

Bir belgeye şablonun nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();

// Microsoft Word belgeleri varsayılan olarak "Normal.dotm" adı verilen bir şablonla birlikte gelir.
// Boş Aspose.Words belgeleri için varsayılan bir şablon yoktur.
Assert.AreEqual(string.Empty, doc.AttachedTemplate);

// Bir şablon ekleyin, ardından stil değişikliklerini uygulamak için bayrağı ayarlayın
// şablon içinde belgemizdeki stillere.
doc.AttachedTemplate = MyDir + "Business brochure.dotx";
doc.AutomaticallyUpdateStyles = true;

doc.Save(ArtifactsDir + "Document.AutomaticallyUpdateStyles.docx");
```

Ekli şablonları olmayan belgeler için varsayılan şablonun nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();

// Otomatik stil güncellemeyi etkinleştirin ancak şablon belgesi eklemeyin.
doc.AutomaticallyUpdateStyles = true;

Assert.AreEqual(string.Empty, doc.AttachedTemplate);

// Şablon belge olmadığından belgenin stil değişikliklerini izleyecek yeri yoktu.
// Şablonu otomatik olarak ayarlamak için SaveOptions nesnesini kullanın
// eğer kaydettiğimiz belgede belge yoksa.
SaveOptions options = SaveOptions.CreateSaveOptions("Document.DefaultTemplate.docx");
options.DefaultTemplate = MyDir + "Business brochure.dotx";

doc.Save(ArtifactsDir + "Document.DefaultTemplate.docx", options);
```

### Ayrıca bakınız

* class [Document](../)
* ad alanı [Aspose.Words](../../document/)
* toplantı [Aspose.Words](../../../)


