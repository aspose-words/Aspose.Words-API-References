---
title: Document.ProtectionType
linktitle: ProtectionType
articleTitle: ProtectionType
second_title: .NET için Aspose.Words
description: Gelişmiş güvenlik ve veri bütünlüğü için etkin belge koruma türünü keşfedin. Gelişmiş özelliklerimizle dosyalarınızı zahmetsizce koruyun.
type: docs
weight: 340
url: /tr/net/aspose.words/document/protectiontype/
---
## Document.ProtectionType property

Şu anda etkin olan belge koruma türünü alır.

```csharp
public ProtectionType ProtectionType { get; }
```

## Notlar

Bu özellik, geçerli olarak ayarlanmış belge koruma türünü almaya olanak tanır. Belge koruma türünü değiştirmek için şunu kullanın:[`Protect`](../protect/) ve[`Unprotect`](../unprotect/) Yöntemler.

Bir belge korunduğunda, kullanıcı yalnızca açıklama ekleme, düzeltme yapma veya bir formu doldurma gibi sınırlı değişiklikler yapabilir.

Belge korumasının yazma korumasından farklı olduğunu unutmayın. Yazma koruması, şunu kullanarak belirtilir:[`WriteProtection`](../writeprotection/)

## Örnekler

Bir belgenin nasıl korunacağını ve korumasının nasıl kaldırılacağını gösterir.

```csharp
Document doc = new Document();
doc.Protect(ProtectionType.ReadOnly, "password");

Assert.AreEqual(ProtectionType.ReadOnly, doc.ProtectionType);

// Bu belgeyi düzenlemeyi amaçlayarak Microsoft Word ile açarsak,
// Korumayı aşabilmek için şifreyi uygulamamız gerekecek.
doc.Save(ArtifactsDir + "Document.Protect.docx");

// Korumanın yalnızca belgemizi açan Microsoft Word kullanıcıları için geçerli olduğunu unutmayın.
// Belgeyi hiçbir şekilde şifrelemedik ve programlı olarak açmak ve düzenlemek için şifreye ihtiyacımız yok.
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

// 2 - Doğru şifre ile:
doc.Unprotect("NewPassword");

Assert.AreEqual(ProtectionType.NoProtection, doc.ProtectionType);
```

### Ayrıca bakınız

* enum [ProtectionType](../../protectiontype/)
* class [Document](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
