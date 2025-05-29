---
title: Field.DisplayResult
linktitle: DisplayResult
articleTitle: DisplayResult
second_title: .NET için Aspose.Words
description: Görüntülenen alan sonuçlarınız için metni ileten, netliği ve kullanıcı deneyimini artıran Field DisplayResult özelliğini keşfedin.
type: docs
weight: 10
url: /tr/net/aspose.words.fields/field/displayresult/
---
## Field.DisplayResult property

Görüntülenen alan sonucunu temsil eden metni alır.

```csharp
public string DisplayResult { get; }
```

## Notlar

[`UpdateListLabels`](../../../aspose.words/document/updatelistlabels/) the için doğru değeri elde etmek için yöntem çağrılmalıdır[`FieldListNum`](../../fieldlistnum/) ,[`FieldAutoNum`](../../fieldautonum/) ,[`FieldAutoNumOut`](../../fieldautonumout/) Ve[`FieldAutoNumLgl`](../../fieldautonumlgl/) alanlar.

## Örnekler

Bir alanın belgede görüntülediği gerçek metnin nasıl alınacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("This document was written by ");
FieldAuthor fieldAuthor = (FieldAuthor)builder.InsertField(FieldType.FieldAuthor, true);
fieldAuthor.AuthorName = "John Doe";

// DisplayResult özelliğini kullanarak tam olarak hangi metnin görüntülendiğini doğrulayabiliriz
// bir alan, belgedeki yerinde görüntülenecektir.
Assert.AreEqual(string.Empty, fieldAuthor.DisplayResult);

 // Alanlar gerçek zamanlı olarak doğru sonuç değerlerini korumaz.
// Alanlarımızın her an doğru sonuçları gösterdiğinden emin olmak için,
// örneğin bir kaydetme işleminden hemen önce bunları manuel olarak güncellememiz gerekiyor.
fieldAuthor.Update();

Assert.AreEqual("John Doe", fieldAuthor.DisplayResult);

doc.Save(ArtifactsDir + "Field.DisplayResult.docx");
```

### Ayrıca bakınız

* class [Field](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)
