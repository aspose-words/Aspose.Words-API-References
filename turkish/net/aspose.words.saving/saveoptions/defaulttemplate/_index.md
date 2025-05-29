---
title: SaveOptions.DefaultTemplate
linktitle: DefaultTemplate
articleTitle: DefaultTemplate
second_title: .NET için Aspose.Words
description: SaveOptions'ınızı kolayca yönetin! Sorunsuz belge işleme için varsayılan şablon yolunu ve dosya adını ayarlayın veya edinin. İş akışınızı bugün optimize edin!
type: docs
weight: 40
url: /tr/net/aspose.words.saving/saveoptions/defaulttemplate/
---
## SaveOptions.DefaultTemplate property

Varsayılan şablona giden yolu alır veya ayarlar (dosya adı dahil). Bu özellik için varsayılan değer**boş dize** (Empty ).

```csharp
public string DefaultTemplate { get; set; }
```

## Notlar

Belirtilirse, bu yol şablonu yüklemek için kullanılır[`AutomaticallyUpdateStyles`](../../../aspose.words/document/automaticallyupdatestyles/) dır`doğru` , ama[`AttachedTemplate`](../../../aspose.words/document/attachedtemplate/) boş.

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

* class [SaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
