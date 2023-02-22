---
title: FileFormatInfo.IsEncrypted
second_title: Aspose.Words for .NET API Referansı
description: FileFormatInfo mülk. Belge şifrelenmişse ve açmak için bir parola gerektiriyorsa true değerini döndürür.
type: docs
weight: 30
url: /tr/net/aspose.words/fileformatinfo/isencrypted/
---
## FileFormatInfo.IsEncrypted property

Belge şifrelenmişse ve açmak için bir parola gerektiriyorsa true değerini döndürür.

```csharp
public bool IsEncrypted { get; }
```

### Notlar

Bu özellik, şifrelenmiş belgeleri olmayanlardan ayırmanıza yardımcı olmak için mevcuttur. Aspose.Words kullanarak şifreli bir belgeyi bir parola sağlamadan yüklemeye çalışırsanız, bir istisnası atılır. Bu özelliği, bir belgenin parolası gerektirip gerektirmediğini saptamak ve bir belgeyi yüklemeden önce bazı eylemler gerçekleştirmek, örneğin kullanıcıdan parola istemek için kullanabilirsiniz.

### Örnekler

Belge biçimini ve şifrelemeyi algılamak için FileFormatUtil sınıfının nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document();

// Belgeyi şifrelemek için bir SaveOptions nesnesi yapılandırın
// kaydettiğimizde bir şifre ile ve ardından belgeyi kaydedin.
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


