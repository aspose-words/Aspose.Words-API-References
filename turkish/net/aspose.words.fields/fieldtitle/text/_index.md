---
title: FieldTitle.Text
linktitle: Text
articleTitle: Text
second_title: .NET için Aspose.Words
description: FieldTitle Text özelliğinizi zahmetsizce yönetin. Uygulamanızda gelişmiş netlik ve kullanıcı deneyimi için başlık metnini kolayca alın veya ayarlayın.
type: docs
weight: 20
url: /tr/net/aspose.words.fields/fieldtitle/text/
---
## FieldTitle.Text property

Başlığın metnini alır veya ayarlar.

```csharp
public string Text { get; set; }
```

## Örnekler

TITLE alanının nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document();

 // "Başlık" yerleşik belge özelliği için bir değer ayarlayın.
doc.BuiltInDocumentProperties.Title = "My Title";

// Bu özelliğin değerini belgede görüntülemek için TITLE alanını kullanabiliriz.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldTitle field = (FieldTitle)builder.InsertField(FieldType.FieldTitle, false);
field.Update();

Assert.AreEqual(" TITLE ", field.GetFieldCode());
Assert.AreEqual("My Title", field.Result);

// Alanın Metin özelliği için bir değer ayarlama,
// ve ardından alanı güncellemek, yeni değerle ilgili yerleşik özelliğin üzerine yazacaktır.
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
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)
