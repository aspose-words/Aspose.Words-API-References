---
title: FileFormatInfo.IsEncrypted
second_title: Aspose.Words for .NET API Referansı
description: FileFormatInfo mülk. İadelerdoğru belge şifrelenmişse ve açmak için şifre gerektiriyorsa.
type: docs
weight: 30
url: /tr/net/aspose.words/fileformatinfo/isencrypted/
---
## FileFormatInfo.IsEncrypted property

İadeler`doğru` belge şifrelenmişse ve açmak için şifre gerektiriyorsa.

```csharp
public bool IsEncrypted { get; }
```

### Notlar

Bu özellik, şifrelenmiş belgeleri şifrelenmemiş olanlardan ayırmanıza yardımcı olmak için mevcuttur. Aspose.Words'ü kullanarak şifrelenmiş bir belgeyi şifre girmeden yüklemeye çalışırsanız, bir istisnası oluşturulur. Bir belgenin parolasını gerektirip gerektirmediğini tespit etmek ve belgeyi yüklemeden önce kullanıcıdan parola istemek gibi bazı eylemler gerçekleştirmek için bu özelliği kullanabilirsiniz.

### Örnekler

Belge biçimini ve şifrelemeyi algılamak için FileFormatUtil sınıfının nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document();

// Belgeyi şifrelemek için SaveOptions nesnesini yapılandırın
// bir şifre ile kaydettiğimizde ve ardından belgeyi kaydettiğimizde.
OdtSaveOptions saveOptions = new OdtSaveOptions(SaveFormat.Odt);
saveOptions.Password = "MyPassword";

doc.Save(ArtifactsDir + "File.DetectDocumentEncryption.odt", saveOptions);

// Belgemizin dosya türünü ve şifreleme durumunu doğrulayın.
FileFormatInfo info = FileFormatUtil.DetectFileFormat(ArtifactsDir + "File.DetectDocumentEncryption.odt");

Assert.AreEqual(".odt", FileFormatUtil.LoadFormatToExtension(info.LoadFormat));
Assert.True(info.IsEncrypted);
```

### Ayrıca bakınız

* class [FileFormatInfo](../)
* ad alanı [Aspose.Words](../../fileformatinfo/)
* toplantı [Aspose.Words](../../../)


