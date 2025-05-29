---
title: FileFormatInfo.HasDigitalSignature
linktitle: HasDigitalSignature
articleTitle: HasDigitalSignature
second_title: .NET için Aspose.Words
description: FileFormatInfo HasDigitalSignature özelliğini keşfedin; belgenizin dijital imza içerip içermediğini hızla kontrol ederek güvenliği ve özgünlüğü artırın.
type: docs
weight: 20
url: /tr/net/aspose.words/fileformatinfo/hasdigitalsignature/
---
## FileFormatInfo.HasDigitalSignature property

Geri Döndürür`doğru`eğer bu belge bir dijital imza içeriyorsa. Bu özellik yalnızca bir belgede dijital imzanın mevcut olduğunu bildirir, ancak imzanın geçerli olup olmadığını belirtmez.

```csharp
public bool HasDigitalSignature { get; }
```

## Notlar

Bu özellik, dijital olarak imzalanmış belgeleri imzalanmamış olanlardan ayırmanıza yardımcı olmak için vardır. Dijital olarak imzalanmış bir belgeyi değiştirmek ve kaydetmek için Aspose.Words'ü kullanırsanız, dijital imza kaybolur. Bu, dijital imzanın bir belgenin gerçekliğini korumak için var olması nedeniyle tasarım gereğidir. Bu özelliği kullanarak, dijital olarak imzalanmış belgeleri normal belgelerle aynı şekilde işlemeden önce tespit edebilir ve dijital imzanın kaybolmasını önlemek için bazı eylemlerde bulunabilirsiniz.

## Örnekler

Belge biçimini ve dijital imzaların varlığını algılamak için FileFormatUtil sınıfının nasıl kullanılacağını gösterir.

```csharp
// Bir belgenin dijital olarak imzalanmadığını doğrulamak için FileFormatInfo örneğini kullanın.
FileFormatInfo info = FileFormatUtil.DetectFileFormat(MyDir + "Document.docx");

Assert.AreEqual(".docx", FileFormatUtil.LoadFormatToExtension(info.LoadFormat));
Assert.False(info.HasDigitalSignature);

CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);
SignOptions signOptions = new SignOptions() { SignTime = DateTime.Now };
DigitalSignatureUtil.Sign(MyDir + "Document.docx", ArtifactsDir + "File.DetectDigitalSignatures.docx",
    certificateHolder, signOptions);

// İmzalandığını doğrulamak için yeni bir FileFormatInstance kullanın.
info = FileFormatUtil.DetectFileFormat(ArtifactsDir + "File.DetectDigitalSignatures.docx");

Assert.True(info.HasDigitalSignature);

// İmzalanmış bir belgenin imzalarını bu şekilde bir koleksiyona yükleyebilir ve erişebiliriz.
Assert.AreEqual(1, DigitalSignatureUtil.LoadSignatures(ArtifactsDir + "File.DetectDigitalSignatures.docx").Count);
```

### Ayrıca bakınız

* class [FileFormatInfo](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
