---
title: DocSaveOptions.SaveFormat
linktitle: SaveFormat
articleTitle: SaveFormat
second_title: .NET için Aspose.Words
description: Sorunsuz belge kaydetme için Doc veya Nokta biçimleri arasında kolayca seçim yapmak üzere DocSaveOptions SaveFormat özelliğini keşfedin. İş akışınızı bugün optimize edin!
type: docs
weight: 50
url: /tr/net/aspose.words.saving/docsaveoptions/saveformat/
---
## DocSaveOptions.SaveFormat property

Bu kaydetme seçenekleri nesnesi kullanılırsa belgenin kaydedileceği biçimi belirtir. Doc veyaDot .

```csharp
public override SaveFormat SaveFormat { get; set; }
```

## Örnekler

Eski Microsoft Word biçimleri için kaydetme seçeneklerinin nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Hello world!");

DocSaveOptions options = new DocSaveOptions(SaveFormat.Doc);

// Microsoft Word veya Aspose.Words ile belgenin yüklenmesini koruyacak bir parola belirleyin.
// Bu işlemin belgenin içeriğini hiçbir şekilde şifrelemediğini unutmayın.
options.Password = "MyPassword";

// Belgede yönlendirme fişi varsa, bu bayrağı true olarak ayarlayarak kaydederken bunu koruyabiliriz.
options.SaveRoutingSlip = true;

doc.Save(ArtifactsDir + "DocSaveOptions.SaveAsDoc.doc", options);

// Belgeyi yükleyebilmek için,
// DocSaveOptions nesnesinde belirttiğimiz şifreyi bir LoadOptions nesnesine uygulamamız gerekecek.
Assert.Throws<IncorrectPasswordException>(() => doc = new Document(ArtifactsDir + "DocSaveOptions.SaveAsDoc.doc"));

LoadOptions loadOptions = new LoadOptions("MyPassword");
doc = new Document(ArtifactsDir + "DocSaveOptions.SaveAsDoc.doc", loadOptions);

Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### Ayrıca bakınız

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [DocSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
