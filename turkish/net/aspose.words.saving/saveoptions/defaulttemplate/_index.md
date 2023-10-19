---
title: SaveOptions.DefaultTemplate
linktitle: DefaultTemplate
articleTitle: DefaultTemplate
second_title: Aspose.Words for .NET
description: SaveOptions DefaultTemplate mülk. Varsayılan şablonun yolunu alır veya ayarlar dosya adı dahil. Bu özellik için varsayılan değerboş dize Empty C#'da.
type: docs
weight: 40
url: /tr/net/aspose.words.saving/saveoptions/defaulttemplate/
---
## SaveOptions.DefaultTemplate property

Varsayılan şablonun yolunu alır veya ayarlar (dosya adı dahil). Bu özellik için varsayılan değer:**boş dize** (Empty).

```csharp
public string DefaultTemplate { get; set; }
```

## Notlar

Belirtilmişse, bu yol aşağıdaki durumlarda şablonu yüklemek için kullanılır:[`AutomaticallyUpdateStyles`](../../../aspose.words/document/automaticallyupdatestyles/) dır-dir`doğru` , ama[`AttachedTemplate`](../../../aspose.words/document/attachedtemplate/) boş.

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

* class [SaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
