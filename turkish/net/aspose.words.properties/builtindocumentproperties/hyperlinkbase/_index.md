---
title: HyperlinkBase
second_title: Aspose.Words for .NET API Referansı
description: Bu belgedeki göreli köprüleri değerlendirmek için kullanılan temel dizeyi belirtir.
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
// Microsoft Word'deki bağlantıya tıklamak, varsa belirtilen belgeyi açacaktır.
builder.InsertHyperlink("Relative hyperlink", "Document.docx", false);

// Bu bağlantı görecelidir. Aynı klasörde "Document.docx" yoksa
// bu bağlantıyı içeren belge olarak bağlantı kopacak.
Assert.False(File.Exists(ArtifactsDir + "Document.docx"));
doc.Save(ArtifactsDir + "DocumentProperties.HyperlinkBase.BrokenLink.docx");

// Bağlanmaya çalıştığımız belge, belgeyi kaydetmeyi planladığımızdan farklı bir dizinde.
// Her birine mutlak bir dosya adı koyarak bunun gibi bağlantıları düzeltebiliriz. 
// Alternatif olarak, her köprünün göreli bir dosya adına sahip olduğu bir temel bağlantı sağlayabiliriz.
// üzerine tıkladığımızda bağlantısının başına gelecek. 
BuiltInDocumentProperties properties = doc.BuiltInDocumentProperties;
properties.HyperlinkBase = MyDir;

Assert.True(File.Exists(properties.HyperlinkBase + ((FieldHyperlink)doc.Range.Fields[0]).Address));

doc.Save(ArtifactsDir + "DocumentProperties.HyperlinkBase.WorkingLink.docx");
```

### Ayrıca bakınız

* class [BuiltInDocumentProperties](../../builtindocumentproperties)
* ad alanı [Aspose.Words.Properties](../../builtindocumentproperties)
* toplantı [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
