---
title: Document.AttachedTemplate
linktitle: AttachedTemplate
articleTitle: AttachedTemplate
second_title: Aspose.Words for .NET
description: Document AttachedTemplate mülk. Belgeye eklenen şablonun tam yolunu alır veya ayarlar C#'da.
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
| ArgumentNullException | Ayarlamaya çalışırsanız fırlatır`hükümsüz` değer. |

## Notlar

Boş dize, belgenin Normal şablona eklendiği anlamına gelir.

## Örnekler

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
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
