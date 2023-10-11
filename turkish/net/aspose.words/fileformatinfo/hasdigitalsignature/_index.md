---
title: FileFormatInfo.HasDigitalSignature
second_title: Aspose.Words for .NET API Referansı
description: FileFormatInfo mülk. İadelerdoğruBu belge dijital imza içeriyorsa. Bu özellik yalnızca bir belgede dijital imzanın bulunduğunu bildirir ancak imzanın geçerli olup olmadığını belirtmez.
type: docs
weight: 20
url: /tr/net/aspose.words/fileformatinfo/hasdigitalsignature/
---
## FileFormatInfo.HasDigitalSignature property

İadeler`doğru`Bu belge dijital imza içeriyorsa. Bu özellik yalnızca bir belgede dijital imzanın bulunduğunu bildirir, ancak imzanın geçerli olup olmadığını belirtmez.

```csharp
public bool HasDigitalSignature { get; }
```

### Notlar

Bu özellik, dijital olarak imzalanmış belgeleri dijital olarak imzalanmamış olanlardan ayırmanıza yardımcı olmak için mevcuttur. Aspose.Words'ü dijital olarak imzalanmış bir belgeyi değiştirmek ve kaydetmek için kullanırsanız, dijital imza kaybolur. Bunun nedeni tasarım gereğidir çünkü bir belgenin orijinalliğini korumak için dijital bir imza mevcuttur. Bu özelliği kullanarak, dijital olarak imzalanmış belgeleri, normal belgelerle aynı şekilde işlemeden önce tespit edebilir ve dijital imzanın kaybolmasını önlemek için kullanıcıya bildirimde bulunmak gibi bazı eylemler gerçekleştirebilirsiniz.

### Örnekler

Belge biçimini ve dijital imzaların varlığını algılamak için FileFormatUtil sınıfının nasıl kullanılacağını gösterir.

```csharp
// Bir belgenin dijital olarak imzalanmadığını doğrulamak için FileFormatInfo örneğini kullanın.
FileFormatInfo info = FileFormatUtil.DetectFileFormat(MyDir + "Document.docx");

Assert.AreEqual(".docx", FileFormatUtil.LoadFormatToExtension(info.LoadFormat));
Assert.False(info.HasDigitalSignature);

CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);
DigitalSignatureUtil.Sign(MyDir + "Document.docx", ArtifactsDir + "File.DetectDigitalSignatures.docx",
    certificateHolder, new SignOptions() { SignTime = DateTime.Now });

// İmzalandığını onaylamak için yeni bir FileFormatInstance kullanın.
info = FileFormatUtil.DetectFileFormat(ArtifactsDir + "File.DetectDigitalSignatures.docx");

Assert.True(info.HasDigitalSignature);

// Bunun gibi bir koleksiyonda imzalı bir belgenin imzalarına yükleyebilir ve erişebiliriz.
Assert.AreEqual(1, DigitalSignatureUtil.LoadSignatures(ArtifactsDir + "File.DetectDigitalSignatures.docx").Count);
```

### Ayrıca bakınız

* class [FileFormatInfo](../)
* ad alanı [Aspose.Words](../../fileformatinfo/)
* toplantı [Aspose.Words](../../../)


