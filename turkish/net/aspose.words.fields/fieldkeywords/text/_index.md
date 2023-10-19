---
title: FieldKeywords.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words for .NET
description: FieldKeywords Text mülk. Anahtar kelimelerin metnini alır veya ayarlar C#'da.
type: docs
weight: 20
url: /tr/net/aspose.words.fields/fieldkeywords/text/
---
## FieldKeywords.Text property

Anahtar kelimelerin metnini alır veya ayarlar.

```csharp
public string Text { get; set; }
```

## Örnekler

ANAHTAR KELİMELER alanının eklenmesini gösterir.

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

// Alanın Text özelliği için bir değer ayarlıyoruz,
// ve ardından alanın güncellenmesi, yeni değerin karşılık gelen yerleşik özelliğin üzerine yazılmasına neden olacaktır.
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
