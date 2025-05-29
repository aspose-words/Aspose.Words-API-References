---
title: PdfEncryptionDetails.UserPassword
linktitle: UserPassword
articleTitle: UserPassword
second_title: .NET için Aspose.Words
description: UserPassword özelliğinin, erişim için parola gerektirmesi sayesinde PDF güvenliğini nasıl artırdığını ve belgelerinizin korunup gizli kalmasını nasıl sağladığını keşfedin.
type: docs
weight: 40
url: /tr/net/aspose.words.saving/pdfencryptiondetails/userpassword/
---
## PdfEncryptionDetails.UserPassword property

Şifrelenmiş PDF belgesini açmak için gereken kullanıcı parolasını belirtir.

```csharp
public string UserPassword { get; set; }
```

## Notlar

Şifrelenmiş bir PDF belgesini görüntülemek için açmak için kullanıcı parolası gerekecektir. Belirtilen izinler in [`Permissions`](../permissions/) okuyucu yazılımı tarafından uygulanacaktır.

Kullanıcı şifresi şu şekilde olabilir:`hükümsüz` veya boş dize, bu durumda kullanıcıdan PDF belgesini açarken parola istenmeyecektir. Kullanıcı parolası, sahip parolasıyla aynı olamaz.

## Örnekler

Kaydedilmiş bir PDF belgesinde izinlerin nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

// Açıklamaların düzenlenmesine izin vermek için izinleri genişletin.
PdfEncryptionDetails encryptionDetails =
    new PdfEncryptionDetails("password", string.Empty, PdfPermissions.ModifyAnnotations | PdfPermissions.DocumentAssembly);

// Belgenin "Kaydet" metoduna geçirebileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'e nasıl dönüştüreceğini değiştirmek için.
PdfSaveOptions saveOptions = new PdfSaveOptions();
// "EncryptionDetails" özelliği aracılığıyla şifrelemeyi etkinleştirin.
saveOptions.EncryptionDetails = encryptionDetails;

// Bu belgeyi açtığımızda, içeriğine erişmeden önce parolayı girmemiz gerekecektir.
doc.Save(ArtifactsDir + "PdfSaveOptions.EncryptionPermissions.pdf", saveOptions);
```

### Ayrıca bakınız

* class [PdfEncryptionDetails](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
