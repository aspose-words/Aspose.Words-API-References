---
title: Document.ProtectionType
linktitle: ProtectionType
articleTitle: ProtectionType
second_title: Aspose.Words for .NET
description: Document ProtectionType mülk. Şu anda etkin olan belge koruma türünü alır C#'da.
type: docs
weight: 330
url: /tr/net/aspose.words/document/protectiontype/
---
## Document.ProtectionType property

Şu anda etkin olan belge koruma türünü alır.

```csharp
public ProtectionType ProtectionType { get; }
```

## Notlar

Bu özellik, halihazırda ayarlanmış olan belge koruma tipinin alınmasına olanak sağlar. Belge koruma tipini değiştirmek için şunu kullanın:[`Protect`](../protect/) ve[`Unprotect`](../unprotect/) yöntemler.

Bir belge korunduğunda, kullanıcı açıklama ekleme, düzeltme yapma veya form doldurma gibi yalnızca sınırlı değişiklikler yapabilir.

Belge korumasının yazma korumasından farklı olduğunu unutmayın. Yazma koruması,[`WriteProtection`](../writeprotection/)

## Örnekler

Bir belgenin nasıl korunacağını ve korumasının nasıl kaldırılacağını gösterir.

```csharp
Document doc = new Document();
doc.Protect(ProtectionType.ReadOnly, "password");

Assert.AreEqual(ProtectionType.ReadOnly, doc.ProtectionType);

// Bu belgeyi düzenlemek amacıyla Microsoft Word ile açarsak,
// korumayı aşmak için şifreyi uygulamamız gerekecek.
doc.Save(ArtifactsDir + "Document.Protect.docx");

// Korumanın yalnızca belgemizi açan Microsoft Word kullanıcıları için geçerli olduğunu unutmayın.
// Belgeyi hiçbir şekilde şifrelemedik ve onu programlı olarak açmak ve düzenlemek için şifreye ihtiyacımız yok.
Document protectedDoc = new Document(ArtifactsDir + "Document.Protect.docx");

Assert.AreEqual(ProtectionType.ReadOnly, protectedDoc.ProtectionType);

DocumentBuilder builder = new DocumentBuilder(protectedDoc);
builder.Writeln("Text added to a protected document.");
// Bir belgeden korumayı kaldırmanın iki yolu vardır.
// 1 - Şifresiz:
doc.Unprotect();

Assert.AreEqual(ProtectionType.NoProtection, doc.ProtectionType);

doc.Protect(ProtectionType.ReadOnly, "NewPassword");

Assert.AreEqual(ProtectionType.ReadOnly, doc.ProtectionType);

doc.Unprotect("WrongPassword");

Assert.AreEqual(ProtectionType.ReadOnly, doc.ProtectionType);

// 2 - Doğru şifreyle:
doc.Unprotect("NewPassword");

Assert.AreEqual(ProtectionType.NoProtection, doc.ProtectionType);
```

### Ayrıca bakınız

* enum [ProtectionType](../../protectiontype/)
* class [Document](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
