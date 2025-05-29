---
title: Document.Unprotect
linktitle: Unprotect
articleTitle: Unprotect
second_title: .NET için Aspose.Words
description: Belge Korumasını Kaldırma yöntemimizle belgelerinizin kilidini kolayca açın, kolay erişim ve düzenleme için tüm parola korumalarını kaldırın.
type: docs
weight: 790
url: /tr/net/aspose.words/document/unprotect/
---
## Unprotect() {#unprotect_1}

Paroladan bağımsız olarak belgenin korumasını kaldırır.

```csharp
public void Unprotect()
```

## Notlar

Bu yöntem, koruma parolası olsa bile belgenin korumasını kaldırır.

Belge korumasının yazma korumasından farklı olduğunu unutmayın. Yazma koruması, şunu kullanarak belirtilir:[`WriteProtection`](../writeprotection/).

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

* class [Document](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)

---

## Unprotect(*string*) {#unprotect}

Doğru bir parola belirtilirse belgeden korumayı kaldırır.

```csharp
public bool Unprotect(string password)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| password | String | Belgenin korumasını kaldırmak için kullanılacak şifre. |

### Geri dönüş değeri

`doğru`eğer doğru bir şifre belirtilmişse ve belge korumasız ise.

## Notlar

Bu yöntem yalnızca doğru bir parola belirtildiği takdirde belgenin korumasını kaldırır.

Belge korumasının yazma korumasından farklı olduğunu unutmayın. Yazma koruması, şunu kullanarak belirtilir:[`WriteProtection`](../writeprotection/).

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

* class [Document](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
