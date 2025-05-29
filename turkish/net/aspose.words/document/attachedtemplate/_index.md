---
title: Document.AttachedTemplate
linktitle: AttachedTemplate
articleTitle: AttachedTemplate
second_title: .NET için Aspose.Words
description: Belge Ekli Şablon özelliğinizi nasıl etkili bir şekilde yöneteceğinizi keşfedin. Sorunsuz entegrasyon için belgenizin şablonunun tam yolunu kolayca ayarlayın veya alın.
type: docs
weight: 20
url: /tr/net/aspose.words/document/attachedtemplate/
---
## Document.AttachedTemplate property

Belgeye eklenen şablonun tam yolunu alır veya ayarlar.

```csharp
public string AttachedTemplate { get; set; }
```

### istisnalar

| istisna | şart |
| --- | --- |
| ArgumentNullException | Bir ayarlamayı denerseniz atar`hükümsüz` değer. |

## Notlar

Boş dize, belgenin Normal şablonuna eklendiği anlamına gelir.

## Örnekler

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
