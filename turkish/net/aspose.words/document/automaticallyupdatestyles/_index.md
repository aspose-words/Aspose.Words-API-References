---
title: Document.AutomaticallyUpdateStyles
linktitle: AutomaticallyUpdateStyles
articleTitle: AutomaticallyUpdateStyles
second_title: .NET için Aspose.Words
description: MS Word'deki AutomaticallyUpdateStyles özelliğinin, belgenizin stillerinin şablonla her açtığınızda senkronize olmasını sağlayarak tutarlılığı nasıl artırdığını keşfedin.
type: docs
weight: 30
url: /tr/net/aspose.words/document/automaticallyupdatestyles/
---
## Document.AutomaticallyUpdateStyles property

Belgedeki stillerin, belge MS Word'de her açıldığında ekli şablondaki stillerle eşleşecek şekilde güncellenip güncellenmeyeceğini belirten bir bayrak alır veya ayarlar.

```csharp
public bool AutomaticallyUpdateStyles { get; set; }
```

## Örnekler

Bir şablonun bir belgeye nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();

// Microsoft Word belgeleri varsayılan olarak "Normal.dotm" adlı ekli bir şablonla birlikte gelir.
// Boş Aspose.Words belgeleri için varsayılan bir şablon yoktur.
Assert.AreEqual(string.Empty, doc.AttachedTemplate);

// Bir şablon ekleyin, ardından stil değişikliklerini uygulamak için bayrağı ayarlayın
// Şablon içerisinde belgemizdeki stillere.
doc.AttachedTemplate = MyDir + "Business brochure.dotx";
doc.AutomaticallyUpdateStyles = true;

doc.Save(ArtifactsDir + "Document.AutomaticallyUpdateStyles.docx");
```

Ekli şablonu olmayan belgeler için varsayılan şablonun nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();

// Otomatik stil güncellemesini etkinleştirin, ancak şablon belge eklemeyin.
doc.AutomaticallyUpdateStyles = true;

Assert.AreEqual(string.Empty, doc.AttachedTemplate);

// Şablon belge olmadığından, belgede stil değişikliklerini izleyecek bir yer yoktu.
// Bir şablonu otomatik olarak ayarlamak için SaveOptions nesnesini kullanın
// eğer kaydettiğimiz bir belgede yoksa.
SaveOptions options = SaveOptions.CreateSaveOptions("Document.DefaultTemplate.docx");
options.DefaultTemplate = MyDir + "Business brochure.dotx";

doc.Save(ArtifactsDir + "Document.DefaultTemplate.docx", options);
```

### Ayrıca bakınız

* class [Document](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
