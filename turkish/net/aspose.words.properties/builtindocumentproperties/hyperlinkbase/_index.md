---
title: BuiltInDocumentProperties.HyperlinkBase
linktitle: HyperlinkBase
articleTitle: HyperlinkBase
second_title: .NET için Aspose.Words
description: Belgelerinizdeki göreli köprü metinlerini kusursuz gezinme ve gelişmiş kullanıcı deneyimi için optimize etmek amacıyla BuiltInDocumentProperties HyperlinkBase özelliğini keşfedin.
type: docs
weight: 120
url: /tr/net/aspose.words.properties/builtindocumentproperties/hyperlinkbase/
---
## BuiltInDocumentProperties.HyperlinkBase property

Bu belgedeki bağıl köprü metinlerini değerlendirmek için kullanılan temel dizeyi belirtir.

```csharp
public string HyperlinkBase { get; set; }
```

## Notlar

Aspose.Words bu özelliği kullanmaz.

## Örnekler

Bir köprü metninin taban kısmının belgenin özelliklerinde nasıl saklanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Yerel dosya sistemindeki "Document.docx" adlı bir belgeye göreli bir köprü metni ekleyin.
// Microsoft Word'deki bağlantıya tıklandığında, varsa belirtilen belge açılacaktır.
builder.InsertHyperlink("Relative hyperlink", "Document.docx", false);

// Bu bağlantı görecelidir. Aynı klasörde "Document.docx" yoksa
// Bu bağlantıyı içeren belge bozulacağından bağlantı kesilecektir.
Assert.False(File.Exists(ArtifactsDir + "Document.docx"));
doc.Save(ArtifactsDir + "DocumentProperties.HyperlinkBase.BrokenLink.docx");

// Bağlanmaya çalıştığımız belge, kaydetmeyi planladığımız dizinden farklı bir dizinde.
 // Her birine kesin bir dosya adı koyarak bu tür bağlantıları düzeltebiliriz.
// Alternatif olarak, her köprü metninin göreceli bir dosya adına sahip olduğu bir temel bağlantı sağlayabiliriz.
 // Üzerine tıkladığımızda bağlantısının önüne eklenecektir.
BuiltInDocumentProperties properties = doc.BuiltInDocumentProperties;
properties.HyperlinkBase = MyDir;

Assert.True(File.Exists(properties.HyperlinkBase + ((FieldHyperlink)doc.Range.Fields[0]).Address));

doc.Save(ArtifactsDir + "DocumentProperties.HyperlinkBase.WorkingLink.docx");
```

### Ayrıca bakınız

* class [BuiltInDocumentProperties](../)
* ad alanı [Aspose.Words.Properties](../../../aspose.words.properties/)
* toplantı [Aspose.Words](../../../)
