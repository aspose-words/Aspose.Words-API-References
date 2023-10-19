---
title: WriteProtection Class
linktitle: WriteProtection
articleTitle: WriteProtection
second_title: Aspose.Words for .NET
description: Aspose.Words.Settings.WriteProtection sınıf. Bir belgenin yazma koruması ayarlarını belirtir C#'da.
type: docs
weight: 5970
url: /tr/net/aspose.words.settings/writeprotection/
---
## WriteProtection class

Bir belgenin yazma koruması ayarlarını belirtir.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Bir Belgeyi Koruyun veya Şifreleyin](https://docs.aspose.com/words/net/protect-or-encrypt-a-document/) dokümantasyon makalesi.

```csharp
public class WriteProtection
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [IsWriteProtected](../../aspose.words.settings/writeprotection/iswriteprotected/) { get; } | İadeler`doğru` yazma koruması şifresi ayarlandığında. |
| [ReadOnlyRecommended](../../aspose.words.settings/writeprotection/readonlyrecommended/) { get; set; } | Belge yazarının belgenin salt okunur olarak açılmasını önerip önermediğini belirtir. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [SetPassword](../../aspose.words.settings/writeprotection/setpassword/)(*string*) | Belgenin yazma koruması parolasını ayarlar. |
| [ValidatePassword](../../aspose.words.settings/writeprotection/validatepassword/)(*string*) | İadeler`doğru` belirtilen parola belgenin korunduğu yazma koruma parolasıyla aynıysa. Belge parolayla yazmaya karşı korumalı değilse o zaman şunu döndürür:`YANLIŞ` . |

## Notlar

Yazma koruması, yazarın belgesinin salt okunur olarak açılmasını ve/veya bir belgeyi değiştirmek için parola gerektirmesini önerip önermediğini belirtir.

Yazma koruması belge korumasından farklıdır. Yazma koruması, Farklı Kaydet iletişim kutusunun seçeneklerinde Microsoft Word'de belirtilmiştir.

Bu sınıfın örneklerini doğrudan oluşturmazsınız. Belge koruma ayarlarına üzerinden erişebilirsiniz.[`WriteProtection`](../../aspose.words/document/writeprotection/) mülk.

## Örnekler

Bir belgenin parolayla nasıl korunacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world! This document is protected.");
// En fazla 15 karakter uzunluğunda bir şifre girin ve ardından belgenin koruma durumunu doğrulayın.
doc.WriteProtection.SetPassword("MyPassword");
doc.WriteProtection.ReadOnlyRecommended = true;

Assert.IsTrue(doc.WriteProtection.IsWriteProtected);
Assert.IsTrue(doc.WriteProtection.ValidatePassword("MyPassword"));

// Koruma, belgenin programlı olarak düzenlenmesini engellemez veya içeriği şifrelemez.
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
