---
title: FieldTitle.Text
second_title: Aspose.Words for .NET API Referansı
description: FieldTitle mülk. Başlığın metnini alır veya ayarlar.
type: docs
weight: 20
url: /tr/net/aspose.words.fields/fieldtitle/text/
---
## FieldTitle.Text property

Başlığın metnini alır veya ayarlar.

```csharp
public string Text { get; set; }
```

### Örnekler

TITLE alanının nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document();

 // "Başlık" yerleşik belge özelliği için bir değer belirleyin.
doc.BuiltInDocumentProperties.Title = "My Title";

// Bu özelliğin değerini belgede görüntülemek için TITLE alanını kullanabiliriz.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldTitle field = (FieldTitle)builder.InsertField(FieldType.FieldTitle, false);
field.Update();

Assert.AreEqual(" TITLE ", field.GetFieldCode());
Assert.AreEqual("My Title", field.Result);

// Alanın Text özelliği için bir değer ayarlıyoruz,
// ve ardından alanın güncellenmesi, yeni değerin karşılık gelen yerleşik özelliğin üzerine yazılmasına neden olacaktır.
builder.Writeln();
field = (FieldTitle)builder.InsertField(FieldType.FieldTitle, false);
field.Text = "My New Title";
field.Update();

Assert.AreEqual(" TITLE  \"My New Title\"", field.GetFieldCode());
Assert.AreEqual("My New Title", field.Result);
Assert.AreEqual("My New Title", doc.BuiltInDocumentProperties.Title);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.TITLE.docx");
```

### Ayrıca bakınız

* class [FieldTitle](../)
* ad alanı [Aspose.Words.Fields](../../fieldtitle/)
* toplantı [Aspose.Words](../../../)


