---
title: FieldKeywords.Text
second_title: Aspose.Words for .NET API Referansı
description: FieldKeywords mülk. Anahtar kelimelerin metnini alır veya ayarlar.
type: docs
weight: 20
url: /tr/net/aspose.words.fields/fieldkeywords/text/
---
## FieldKeywords.Text property

Anahtar kelimelerin metnini alır veya ayarlar.

```csharp
public string Text { get; set; }
```

### Örnekler

ANAHTAR KELİMELER alanı eklemeyi gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Dosya Gezgini'nde "etiketler" olarak da adlandırılan bazı anahtar kelimeler ekleyin.
doc.BuiltInDocumentProperties.Keywords = "Keyword1, Keyword2";

// ANAHTAR KELİMELER alanı bu özelliğin değerini görüntüler.
FieldKeywords field = (FieldKeywords)builder.InsertField(FieldType.FieldKeyword, true);
field.Update();

Assert.AreEqual(" KEYWORDS ", field.GetFieldCode());
Assert.AreEqual("Keyword1, Keyword2", field.Result);

// Alanın Text özelliği için bir değer ayarlama,
// ve ardından alanı güncellemek, ilgili yerleşik özelliğin üzerine yeni değeri yazacaktır.
field.Text = "OverridingKeyword";
field.Update();

Assert.AreEqual(" KEYWORDS  OverridingKeyword", field.GetFieldCode());
Assert.AreEqual("OverridingKeyword", field.Result);
Assert.AreEqual("OverridingKeyword", doc.BuiltInDocumentProperties.Keywords);

doc.Save(ArtifactsDir + "Field.KEYWORDS.docx");
```

### Ayrıca bakınız

* class [FieldKeywords](../)
* ad alanı [Aspose.Words.Fields](../../fieldkeywords/)
* toplantı [Aspose.Words](../../../)


