---
title: ContentDisposition Enum
linktitle: ContentDisposition
articleTitle: ContentDisposition
second_title: .NET için Aspose.Words
description: Gelişmiş istemci tarayıcı deneyimleri için çeşitli belge sunum seçeneklerini keşfetmek üzere Aspose.Words.ContentDisposition enumunu inceleyin.
type: docs
weight: 540
url: /tr/net/aspose.words/contentdisposition/
---
## ContentDisposition enumeration

Belgenin istemci tarayıcısında sunulmasının farklı yollarını sıralar.

```csharp
public enum ContentDisposition
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Attachment | `0` | Belgeyi tarayıcıya gönder ve belgeyi diske kaydetme veya belgenin uzantısıyla ilişkili uygulamada açma seçeneği sun . |
| Inline | `1` | Belgeyi tarayıcıya gönderir ve belgeyi diske kaydetme veya tarayıcının içinde açma seçeneği sunar. |

## Notlar

İstemci tarayıcısındaki gerçek davranışın, tarayıcının güvenlik yapılandırmasından etkilenebileceğini unutmayın.

## Örnekler

Posta birleştirmenin nasıl gerçekleştirileceğini ve ardından belgenin istemci tarayıcısına nasıl kaydedileceğini gösterir.

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
//Testte HttpResponse boş olduğu için atıldı.
Assert.Throws<ArgumentNullException>(() => doc.Save(response, "Artifacts/MailMerge.ExecuteArray.docx", ContentDisposition.Inline, null));

// Kaydedildikten sonra belgeye gereksiz içerik eklememek için bu yanıtı manuel olarak kapatmamız gerekecek.
Assert.Throws<NullReferenceException>(() => response.End());
```

### Ayrıca bakınız

* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)
