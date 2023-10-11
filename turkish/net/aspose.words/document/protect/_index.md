---
title: Document.Protect
second_title: Aspose.Words for .NET API Referansı
description: Document yöntem. Mevcut şifreyi değiştirmeden belgeyi değişikliklere karşı korur veya rastgele bir şifre atar.
type: docs
weight: 670
url: /tr/net/aspose.words/document/protect/
---
## Protect(ProtectionType) {#protect}

Mevcut şifreyi değiştirmeden belgeyi değişikliklere karşı korur veya rastgele bir şifre atar.

```csharp
public void Protect(ProtectionType type)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| type | ProtectionType | Belgenin koruma türünü belirtir. |

### Notlar

Bir belge korunduğunda, kullanıcı açıklama ekleme, düzeltme yapma veya form doldurma gibi yalnızca sınırlı değişiklikler yapabilir.

Bir belgeyi koruduğunuzda ve belgenin zaten bir koruma parolası varsa, mevcut koruma parolası değişmez.

Bir belgeyi koruduğunuzda ve belgenin bir koruma parolası yoksa, bu yöntem, Microsoft Word'de belgenin korumasını kaldırmayı imkansız hale getiren rastgele bir parola atar, ancak yine de Aspose.Words'de belgenin korumasını kaldırabilirsiniz, çünkü böyle bir şey yoktur korumayı kaldırırken şifre gerektirir.

### Örnekler

Bir bölüm için korumanın nasıl kapatılacağını gösterir.

```csharp
Document doc = new Document();

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Section 1. Hello world!");
builder.InsertBreak(BreakType.SectionBreakNewPage);

builder.Writeln("Section 2. Hello again!");
builder.Write("Please enter text here: ");
builder.InsertTextInput("TextInput1", TextFormFieldType.Regular, "", "Placeholder text", 0);

// Belgedeki her bölüme yazma koruması uygulayın.
doc.Protect(ProtectionType.AllowOnlyFormFields);

// İlk bölüm için yazma korumasını kapatın.
doc.Sections[0].ProtectedForForms = false;

// Bu çıktı belgesinde ilk bölümü serbestçe düzenleyebileceğiz,
// ve ikinci bölümde sadece form alanının içeriğini düzenleyebileceğiz.
doc.Save(ArtifactsDir + "Section.Protect.docx");
```

### Ayrıca bakınız

* enum [ProtectionType](../../protectiontype/)
* class [Document](../)
* ad alanı [Aspose.Words](../../document/)
* toplantı [Aspose.Words](../../../)

---

## Protect(ProtectionType, string) {#protect_1}

Belgeyi değişikliklere karşı korur ve isteğe bağlı olarak bir koruma parolası ayarlar.

```csharp
public void Protect(ProtectionType type, string password)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| type | ProtectionType | Belgenin koruma türünü belirtir. |
| password | String | Belgeyi koruma parolası. Belirtin`hükümsüz`veya belgeyi parola olmadan korumak istiyorsanız boş dize. |

### Notlar

Bir belge korunduğunda, kullanıcı açıklama ekleme, düzeltme yapma veya form doldurma gibi yalnızca sınırlı değişiklikler yapabilir.

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

* enum [ProtectionType](../../protectiontype/)
* class [Document](../)
* ad alanı [Aspose.Words](../../document/)
* toplantı [Aspose.Words](../../../)


