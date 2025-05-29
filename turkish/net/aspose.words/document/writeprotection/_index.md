---
title: Document.WriteProtection
linktitle: WriteProtection
articleTitle: WriteProtection
second_title: .NET için Aspose.Words
description: Belgenizin yazma koruması ayarlarını zahmetsizce yönetmek ve güvenliği artırmak için Belge Yazma Koruması özelliğini keşfedin.
type: docs
weight: 520
url: /tr/net/aspose.words/document/writeprotection/
---
## Document.WriteProtection property

Belge yazma koruması seçeneklerine erişim sağlar.

```csharp
public WriteProtection WriteProtection { get; }
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

* class [WriteProtection](../../../aspose.words.settings/writeprotection/)
* class [Document](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
