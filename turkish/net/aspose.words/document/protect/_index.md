---
title: Document.Protect
linktitle: Protect
articleTitle: Protect
second_title: .NET için Aspose.Words
description: Belgelerinizi Document Protect ile zahmetsizce güvence altına alın. Mevcut parolanızı olduğu gibi korurken veya rastgele bir parola kullanarak yetkisiz değişiklikleri önleyin.
type: docs
weight: 690
url: /tr/net/aspose.words/document/protect/
---
## Protect(*[ProtectionType](../../protectiontype/)*) {#protect}

Mevcut parolayı değiştirmeden belgeyi değişikliklere karşı korur veya rastgele bir parola atar.

```csharp
public void Protect(ProtectionType type)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| type | ProtectionType | Belge için koruma türünü belirtir. |

## Notlar

Bir belge korunduğunda, kullanıcı yalnızca açıklama ekleme, düzeltme yapma veya bir formu doldurma gibi sınırlı değişiklikler yapabilir.

Bir belgeyi koruduğunuzda ve belgenin zaten bir koruma parolası varsa, mevcut koruma parolası değiştirilmez.

Bir belgeyi koruduğunuzda ve belgenin bir koruma parolası yoksa, bu yöntem, Microsoft Word'de belgenin korumasının kaldırılmasını imkansız kılan rastgele bir parola atar. Ancak, Aspose.Words'de belgenin koruması kaldırılabilir çünkü koruma kaldırılırken parola gerekmez.

## Örnekler

Bir bölüm için korumanın nasıl kapatılacağını gösterir.

```csharp
Document doc = new Document();

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Section 1. Hello world!");
builder.InsertBreak(BreakType.SectionBreakNewPage);

builder.Writeln("Section 2. Hello again!");
builder.Write("Please enter text here: ");
builder.InsertTextInput("TextInput1", TextFormFieldType.Regular, "", "Placeholder text", 0);

// Belgedeki her bölüme yazma koruması uygula.
doc.Protect(ProtectionType.AllowOnlyFormFields);

// İlk bölüm için yazma korumasını kapatın.
doc.Sections[0].ProtectedForForms = false;

// Bu çıktı belgesinde, ilk bölümü serbestçe düzenleyebileceğiz,
// ve sadece ikinci bölümdeki form alanının içeriğini düzenleyebileceğiz.
doc.Save(ArtifactsDir + "Section.Protect.docx");
```

### Ayrıca bakınız

* enum [ProtectionType](../../protectiontype/)
* class [Document](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)

---

## Protect(*[ProtectionType](../../protectiontype/), string*) {#protect_1}

Belgeyi değişikliklere karşı korur ve isteğe bağlı olarak bir koruma parolası ayarlar.

```csharp
public void Protect(ProtectionType type, string password)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| type | ProtectionType | Belge için koruma türünü belirtir. |
| password | String | Belgeyi korumak için parola. Belirtin`hükümsüz` veya belgeyi şifresiz korumak istiyorsanız boş bir dize. |

## Notlar

Bir belge korunduğunda, kullanıcı yalnızca açıklama ekleme, düzeltme yapma veya bir formu doldurma gibi sınırlı değişiklikler yapabilir.

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

* enum [ProtectionType](../../protectiontype/)
* class [Document](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
