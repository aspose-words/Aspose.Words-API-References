---
title: WriteProtection Class
linktitle: WriteProtection
articleTitle: WriteProtection
second_title: .NET için Aspose.Words
description: Belge yazma koruması ayarlarını kolayca yönetmek ve belge güvenliğinizi artırmak için Aspose.Words.Settings.WriteProtection sınıfını keşfedin.
type: docs
weight: 6800
url: /tr/net/aspose.words.settings/writeprotection/
---
## WriteProtection class

Bir belge için yazma koruması ayarlarını belirtir.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Bir Belgeyi Koruyun veya Şifreleyin](https://docs.aspose.com/words/net/protect-or-encrypt-a-document/) belgeleme makalesi.

```csharp
public class WriteProtection
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [IsWriteProtected](../../aspose.words.settings/writeprotection/iswriteprotected/) { get; } | Geri Döndürür`doğru` yazma koruması parolası ayarlandığında. |
| [ReadOnlyRecommended](../../aspose.words.settings/writeprotection/readonlyrecommended/) { get; set; } | Belge yazarının belgenin salt okunur olarak açılmasını tavsiye edip etmediğini belirtir. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [SetPassword](../../aspose.words.settings/writeprotection/setpassword/)(*string*) | Belge için yazma koruması parolasını ayarlar. |
| [ValidatePassword](../../aspose.words.settings/writeprotection/validatepassword/)(*string*) | Geri Döndürür`doğru` belirtilen parola, belgenin korunduğu yazma koruması parolasıyla aynıysa. Belge parola ile yazmaya karşı korumalı değilse, şunu döndürür:`YANLIŞ` . |

## Notlar

Yazma koruması, yazarın belgenin salt okunur olarak açılmasını ve/veya belgeyi değiştirmek için parola gerektirilmesini önerdiğini belirtir.

Yazma koruması, belge korumasından farklıdır. Yazma koruması, Microsoft Word'de Farklı Kaydet iletişim kutusunun seçeneklerinde belirtilir.

Bu sınıfın örneklerini doğrudan oluşturmazsınız. Belge koruma ayarlarına şu şekilde erişirsiniz:[`WriteProtection`](../../aspose.words/document/writeprotection/) mülk.

## Örnekler

Bir belgenin parola ile nasıl korunacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world! This document is protected.");
// En fazla 15 karakter uzunluğunda bir parola girin ve ardından belgenin koruma durumunu doğrulayın.
doc.WriteProtection.SetPassword("MyPassword");
doc.WriteProtection.ReadOnlyRecommended = true;

Assert.IsTrue(doc.WriteProtection.IsWriteProtected);
Assert.IsTrue(doc.WriteProtection.ValidatePassword("MyPassword"));

// Koruma, belgenin programlı olarak düzenlenmesini engellemez veya içeriğini şifrelemez.
doc.Save(ArtifactsDir + "Document.WriteProtection.docx");
doc = new Document(ArtifactsDir + "Document.WriteProtection.docx");

Assert.IsTrue(doc.WriteProtection.IsWriteProtected);

builder = new DocumentBuilder(doc);
builder.MoveToDocumentEnd();
builder.Writeln("Writing text in a protected document.");

Assert.AreEqual("Hello world! This document is protected." +
                "\rWriting text in a protected document.", doc.GetText().Trim());
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Settings](../../aspose.words.settings/)
* toplantı [Aspose.Words](../../)
