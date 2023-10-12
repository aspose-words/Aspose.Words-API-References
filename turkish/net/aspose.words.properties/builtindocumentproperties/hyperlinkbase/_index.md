---
title: BuiltInDocumentProperties.HyperlinkBase
second_title: Aspose.Words for .NET API Referansı
description: BuiltInDocumentProperties mülk. Bu belgedeki göreli köprüleri değerlendirmek için kullanılan temel dizeyi belirtir.
type: docs
weight: 120
url: /tr/net/aspose.words.properties/builtindocumentproperties/hyperlinkbase/
---
## BuiltInDocumentProperties.HyperlinkBase property

Bu belgedeki göreli köprüleri değerlendirmek için kullanılan temel dizeyi belirtir.

```csharp
public string HyperlinkBase { get; set; }
```

### Notlar

Aspose.Words bu özelliği kullanmaz.

### Örnekler

Bir köprünün temel kısmının belgenin özelliklerinde nasıl saklanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Yerel dosya sistemindeki "Document.docx" adlı bir belgeye göreli bir köprü ekleyin.
// Microsoft Word'deki bağlantıya tıklamak, varsa belirlenen belgeyi açacaktır.
builder.InsertHyperlink("Relative hyperlink", "Document.docx", false);

// Bu bağlantı görecelidir. Aynı klasörde "Document.docx" yoksa
// bu bağlantıyı içeren belge olarak bağlantı kopacaktır.
Assert.False(File.Exists(ArtifactsDir + "Document.docx"));
doc.Save(ArtifactsDir + "DocumentProperties.HyperlinkBase.BrokenLink.docx");

// Bağlanmaya çalıştığımız belge, belgeyi kaydetmeyi planladığımız dizinden farklı bir dizinde.
 // Bunun gibi bağlantıları her birine mutlak bir dosya adı koyarak düzeltebiliriz.
// Alternatif olarak, her köprünün göreceli bir dosya adına sahip olduğu bir temel bağlantı sağlayabiliriz
 // tıkladığımızda linkin başına eklenecek.
BuiltInDocumentProperties properties = doc.BuiltInDocumentProperties;
properties.HyperlinkBase = MyDir;

Assert.True(File.Exists(properties.HyperlinkBase + ((FieldHyperlink)doc.Range.Fields[0]).Address));

doc.Save(ArtifactsDir + "DocumentProperties.HyperlinkBase.WorkingLink.docx");
```

### Ayrıca bakınız

* class [BuiltInDocumentProperties](../)
* ad alanı [Aspose.Words.Properties](../../builtindocumentproperties/)
* toplantı [Aspose.Words](../../../)


