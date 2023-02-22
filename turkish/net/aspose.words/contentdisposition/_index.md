---
title: Enum ContentDisposition
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.ContentDisposition Sıralama. Belgeyi istemci tarayıcısında sunmanın farklı yollarını sıralar.
type: docs
weight: 330
url: /tr/net/aspose.words/contentdisposition/
---
## ContentDisposition enumeration

Belgeyi istemci tarayıcısında sunmanın farklı yollarını sıralar.

```csharp
public enum ContentDisposition
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Attachment | `0` | Belgeyi tarayıcıya gönderin ve belgeyi diske kaydetme veya belgenin uzantısıyla ilişkili application içinde açma seçeneği sunun. |
| Inline | `1` | Belgeyi tarayıcıya gönderin ve belgeyi diske kaydetme veya tarayıcının içinde açma seçeneği sunar. |

### Notlar

İstemci tarayıcısındaki fiili davranışın, tarayıcının güvenlik yapılandırmasından etkilenebileceğini unutmayın.

### Örnekler

Adres mektup birleştirmenin nasıl gerçekleştirileceğini ve ardından belgenin istemci tarayıcısına nasıl kaydedileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField(" MERGEFIELD FullName ");
builder.InsertParagraph();
builder.InsertField(" MERGEFIELD Company ");
builder.InsertParagraph();
builder.InsertField(" MERGEFIELD Address ");
builder.InsertParagraph();
builder.InsertField(" MERGEFIELD City ");

doc.MailMerge.Execute(new string[] { "FullName", "Company", "Address", "City" },
    new object[] { "James Bond", "MI5 Headquarters", "Milbank", "London" });

// Belgeyi istemci tarayıcısına gönder.
Assert.That(() => doc.Save(response, "Artifacts/MailMerge.ExecuteArray.docx", ContentDisposition.Inline, null),
    Throws.TypeOf<ArgumentNullException>()); //HttpResponse testte boş olduğu için atıldı.

// Kaydettikten sonra belgeye gereksiz içerik eklemediğimizden emin olmak için bu yanıtı manuel olarak kapatmamız gerekecek.
Assert.That(() => response.End(), Throws.TypeOf<NullReferenceException>());
```

### Ayrıca bakınız

* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)


