---
title: FileFormatInfo.IsEncrypted
linktitle: IsEncrypted
articleTitle: IsEncrypted
second_title: .NET için Aspose.Words
description: Belgenizin güvenli olup olmadığını FileFormatInfo IsEncrypted özelliğiyle öğrenin; şifrelenmiş dosyalara erişmek için parola gerektiğinde true değerini döndürür.
type: docs
weight: 40
url: /tr/net/aspose.words/fileformatinfo/isencrypted/
---
## FileFormatInfo.IsEncrypted property

Geri Döndürür`doğru` belge şifrelenmişse ve açmak için parola gerekiyorsa.

```csharp
public bool IsEncrypted { get; }
```

## Notlar

Bu özellik, şifrelenmiş belgeleri şifrelenmemiş olanlardan ayırmanıza yardımcı olmak için vardır. Şifrelenmiş bir belgeyi parola sağlamadan Aspose.Words kullanarak yüklemeye çalışırsanız an istisnası atılır. Bu özelliği, bir belgenin password gerektirip gerektirmediğini tespit etmek ve bir belgeyi yüklemeden önce bazı eylemlerde bulunmak için kullanabilirsiniz, örneğin kullanıcıdan parola istemek.

## Örnekler

Belge biçimini ve şifrelemeyi algılamak için FileFormatUtil sınıfının nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document();

// Belgeyi şifrelemek için bir SaveOptions nesnesi yapılandırın
// kaydederken bir şifre ile kaydediyoruz ve ardından belgeyi kaydediyoruz.
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
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
