---
title: WriteProtection.SetPassword
second_title: Aspose.Words for .NET API Referansı
description: WriteProtection yöntem. Belge için yazma koruması parolasını ayarlar.
type: docs
weight: 30
url: /tr/net/aspose.words.settings/writeprotection/setpassword/
---
## WriteProtection.SetPassword method

Belge için yazma koruması parolasını ayarlar.

```csharp
public void SetPassword(string password)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| password | String | Ayarlanacak parola. Null olamaz, ancak boş bir dize olabilir. |

### Notlar

Bir parola belirlenirse, Microsoft Word, kullanıcının parolayı girmesini veya belgeyi salt okunur olarak açmasını ister.

### Örnekler

Bir belgenin parolayla nasıl korunacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world! This document is protected.");

// En fazla 15 karakter uzunluğunda bir parola girin ve ardından belgenin koruma durumunu doğrulayın.
doc.WriteProtection.SetPassword("MyPassword");
doc.WriteProtection.ReadOnlyRecommended = true;

Assert.IsTrue(doc.WriteProtection.IsWriteProtected);
Assert.IsTrue(doc.WriteProtection.ValidatePassword("MyPassword"));

// Koruma, belgenin programlı olarak düzenlenmesini engellemez ve içeriği şifrelemez.
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

* class [WriteProtection](../)
* ad alanı [Aspose.Words.Settings](../../writeprotection/)
* toplantı [Aspose.Words](../../../)


