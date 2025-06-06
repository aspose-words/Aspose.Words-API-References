---
title: FieldFileSize.IsInKilobytes
linktitle: IsInKilobytes
articleTitle: IsInKilobytes
second_title: .NET için Aspose.Words
description: FieldFileSize IsInKilobytes ile dosya boyutu gösterimini kontrol edin. Gelişmiş veri yönetimi için kilobayt cinsinden boyut görünürlüğünü kolayca değiştirin.
type: docs
weight: 20
url: /tr/net/aspose.words.fields/fieldfilesize/isinkilobytes/
---
## FieldFileSize.IsInKilobytes property

Dosya boyutunun kilobayt olarak gösterilip gösterilmeyeceğini alır veya ayarlar.

```csharp
public bool IsInKilobytes { get; set; }
```

## Örnekler

FILESIZE alanıyla bir belgenin dosya boyutunun nasıl görüntüleneceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Document.docx");

Assert.AreEqual(18105, doc.BuiltInDocumentProperties.Bytes);

DocumentBuilder builder = new DocumentBuilder(doc);
builder.MoveToDocumentEnd();
builder.InsertParagraph();

// Aşağıda üç farklı ölçü birimi bulunmaktadır
// FILESIZE alanlarının belgenin dosya boyutunu gösterebileceği alan.
// 1 - Bayt:
FieldFileSize field = (FieldFileSize)builder.InsertField(FieldType.FieldFileSize, true);
field.Update();

Assert.AreEqual(" FILESIZE ", field.GetFieldCode());
Assert.AreEqual("18105", field.Result);

// 2 - Kilobayt:
builder.InsertParagraph();
field = (FieldFileSize)builder.InsertField(FieldType.FieldFileSize, true);
field.IsInKilobytes = true;
field.Update();

Assert.AreEqual(" FILESIZE  \\k", field.GetFieldCode());
Assert.AreEqual("18", field.Result);

// 3 - Megabayt:
builder.InsertParagraph();
field = (FieldFileSize)builder.InsertField(FieldType.FieldFileSize, true);
field.IsInMegabytes = true;
field.Update();

Assert.AreEqual(" FILESIZE  \\m", field.GetFieldCode());
Assert.AreEqual("0", field.Result);

// Microsoft Word'de düzenleme yaparken bu alanların değerlerini güncellemek için,
// Öncelikle değişiklikleri kaydetmeli ve daha sonra bu alanları manuel olarak güncellemeliyiz.
doc.Save(ArtifactsDir + "Field.FILESIZE.docx");
```

### Ayrıca bakınız

* class [FieldFileSize](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)
