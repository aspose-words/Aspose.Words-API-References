---
title: WriteProtection.ValidatePassword
linktitle: ValidatePassword
articleTitle: ValidatePassword
second_title: .NET için Aspose.Words
description: Belgelerinizi WriteProtection ValidatePassword yöntemiyle güvenceye alın. Gelişmiş güvenlik için parolanın belgenin korumasıyla eşleşip eşleşmediğini kolayca doğrulayın.
type: docs
weight: 40
url: /tr/net/aspose.words.settings/writeprotection/validatepassword/
---
## WriteProtection.ValidatePassword method

Geri Döndürür`doğru` belirtilen parola, belgenin korunduğu yazma koruması parolasıyla aynıysa. Belge parola ile yazmaya karşı korumalı değilse, şunu döndürür:`YANLIŞ` .

```csharp
public bool ValidatePassword(string password)
```

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

* class [WriteProtection](../)
* ad alanı [Aspose.Words.Settings](../../../aspose.words.settings/)
* toplantı [Aspose.Words](../../../)
