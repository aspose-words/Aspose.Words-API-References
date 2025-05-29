---
title: FieldComments.Text
linktitle: Text
articleTitle: Text
second_title: .NET için Aspose.Words
description: FieldComments Text özelliğiyle yorumlarınızı zahmetsizce yönetin; gelişmiş kullanıcı etkileşimi için yorum metnini kolayca alın veya ayarlayın.
type: docs
weight: 20
url: /tr/net/aspose.words.fields/fieldcomments/text/
---
## FieldComments.Text property

Yorumların metnini alır veya ayarlar.

```csharp
public string Text { get; set; }
```

## Örnekler

YORUMLAR alanının nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Belgenin "Yorumlar" yerleşik özelliği için bir değer ayarlayın.
doc.BuiltInDocumentProperties.Comments = "My comment.";

// Yerleşik özelliğin değerini görüntülemek için bir YORUMLAR alanı oluşturun.
FieldComments field = (FieldComments)builder.InsertField(FieldType.FieldComments, true);
field.Update();

Assert.AreEqual(" COMMENTS ", field.GetFieldCode());
Assert.AreEqual("My comment.", field.Result);

// COMMENTS alanının Text özellik değerini verip güncellersek, alan
// "Yorumlar" yerleşik özelliğinin geçerli değerini, Metin özelliğinin değeriyle üzerine yaz,
// ve ardından yeni değeri göster.
field.Text = "My overriding comment.";
field.Update();

Assert.AreEqual(" COMMENTS  \"My overriding comment.\"", field.GetFieldCode());
Assert.AreEqual("My overriding comment.", field.Result);

doc.Save(ArtifactsDir + "Field.COMMENTS.docx");
```

### Ayrıca bakınız

* class [FieldComments](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)
