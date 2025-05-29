---
title: FieldKeywords.Text
linktitle: Text
articleTitle: Text
second_title: .NET için Aspose.Words
description: FieldKeywords'lerinizi kolaylıkla yönetin! Optimum SEO performansı ve gelişmiş görünürlük için anahtar kelime metnine erişin ve özelleştirin.
type: docs
weight: 20
url: /tr/net/aspose.words.fields/fieldkeywords/text/
---
## FieldKeywords.Text property

Anahtar sözcüklerin metnini alır veya ayarlar.

```csharp
public string Text { get; set; }
```

## Örnekler

ANAHTAR KELİMELER alanı eklemek için kullanılır.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Dosya Gezgini'nde "etiketler" olarak da adlandırılan bazı anahtar sözcükler ekleyin.
doc.BuiltInDocumentProperties.Keywords = "Keyword1, Keyword2";

// ANAHTAR KELİMELER alanı bu özelliğin değerini görüntüler.
FieldKeywords field = (FieldKeywords)builder.InsertField(FieldType.FieldKeyword, true);
field.Update();

Assert.AreEqual(" KEYWORDS ", field.GetFieldCode());
Assert.AreEqual("Keyword1, Keyword2", field.Result);

// Alanın Metin özelliği için bir değer ayarlama,
// ve ardından alanı güncellemek, yeni değerle ilgili yerleşik özelliğin üzerine yazacaktır.
field.Text = "OverridingKeyword";
field.Update();

Assert.AreEqual(" KEYWORDS  OverridingKeyword", field.GetFieldCode());
Assert.AreEqual("OverridingKeyword", field.Result);
Assert.AreEqual("OverridingKeyword", doc.BuiltInDocumentProperties.Keywords);

doc.Save(ArtifactsDir + "Field.KEYWORDS.docx");
```

### Ayrıca bakınız

* class [FieldKeywords](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)
