---
title: WriteProtection.IsWriteProtected
second_title: Aspose.Words for .NET API Referansı
description: WriteProtection mülk. İadelerdoğru yazma koruması şifresi ayarlandığında.
type: docs
weight: 10
url: /tr/net/aspose.words.settings/writeprotection/iswriteprotected/
---
## WriteProtection.IsWriteProtected property

İadeler`doğru` yazma koruması şifresi ayarlandığında.

```csharp
public bool IsWriteProtected { get; }
```

### Örnekler

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

* class [WriteProtection](../)
* ad alanı [Aspose.Words.Settings](../../writeprotection/)
* toplantı [Aspose.Words](../../../)


