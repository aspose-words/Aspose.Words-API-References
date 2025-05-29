---
title: Font.SizeBi
linktitle: SizeBi
articleTitle: SizeBi
second_title: .NET için Aspose.Words
description: Sağdan sola belgeler için yazı tipi boyutunu zahmetsizce ayarlayın. Kullanımı kolay Font SizeBi özelliğimizle okunabilirliği ve tasarımı geliştirin!
type: docs
weight: 360
url: /tr/net/aspose.words/font/sizebi/
---
## Font.SizeBi property

Sağdan sola bir belgede kullanılan yazı tipi boyutunu noktalar halinde alır veya ayarlar.

```csharp
public double SizeBi { get; set; }
```

## Örnekler

Sağdan sola ve sağdan sola metinler için ayrı yazı tipi ayarları kümelerinin nasıl tanımlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Soldan sağa metin için bir dizi yazı tipi ayarı tanımlayın.
builder.Font.Name = "Courier New";
builder.Font.Size = 16;
builder.Font.Italic = false;
builder.Font.Bold = false;
builder.Font.LocaleId = new CultureInfo("en-US", false).LCID;

// Sağdan sola metin için başka bir yazı tipi ayarları kümesi tanımlayın.
builder.Font.NameBi = "Andalus";
builder.Font.SizeBi = 24;
builder.Font.ItalicBi = true;
builder.Font.BoldBi = true;
builder.Font.LocaleIdBi = new CultureInfo("ar-AR", false).LCID;

// Eklemek üzere olduğumuz metnin Bidi bayrağını kullanarak gösterilip gösterilmeyeceğini belirtebiliriz.
// belge oluşturucu sağdan soladır. Bu bayrak true olarak ayarlandığında metin eklediğimizde,
// sağdan sola doğru olan yazı tipi ayarları kullanılarak biçimlendirilecektir.
builder.Font.Bidi = true;
builder.Write("مرحبًا");

// Bayrağı false olarak ayarlayın ve ardından soldan sağa metin ekleyin.
// Belge oluşturucu bunları soldan sağa doğru olan yazı tipi ayarlarını kullanarak biçimlendirecektir.
builder.Font.Bidi = false;
builder.Write(" Hello world!");

doc.Save(ArtifactsDir + "Font.Bidi.docx");
```

### Ayrıca bakınız

* class [Font](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
