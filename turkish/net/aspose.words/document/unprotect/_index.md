---
title: Document.Unprotect
second_title: Aspose.Words for .NET API Referansı
description: Document yöntem. Paroladan bağımsız olarak belgedeki korumayı kaldırır.
type: docs
weight: 760
url: /tr/net/aspose.words/document/unprotect/
---
## Unprotect() {#unprotect_1}

Paroladan bağımsız olarak belgedeki korumayı kaldırır.

```csharp
public void Unprotect()
```

### Notlar

Bu yöntem, koruma parolası olsa bile belgenin korumasını kaldırır.

Belge korumasının yazma korumasından farklı olduğunu unutmayın. Yazma koruması,[`WriteProtection`](../writeprotection/).

### Örnekler

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

* class [Document](../)
* ad alanı [Aspose.Words](../../document/)
* toplantı [Aspose.Words](../../../)

---

## Unprotect(string) {#unprotect}

Doğru parola belirtilirse belgedeki korumayı kaldırır.

```csharp
public bool Unprotect(string password)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| password | String | Belgenin korumasını kaldırmak için kullanılan parola. |

### Geri dönüş değeri

`doğru` doğru bir parola belirtildiyse ve belge korumasızsa.

### Notlar

Bu yöntem yalnızca doğru parola belirtildiğinde belgenin korumasını kaldırır.

Belge korumasının yazma korumasından farklı olduğunu unutmayın. Yazma koruması,[`WriteProtection`](../writeprotection/).

### Örnekler

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

* class [Document](../)
* ad alanı [Aspose.Words](../../document/)
* toplantı [Aspose.Words](../../../)


