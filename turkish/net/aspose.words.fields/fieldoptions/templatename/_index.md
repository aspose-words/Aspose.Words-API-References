---
title: FieldOptions.TemplateName
second_title: Aspose.Words for .NET API Referansı
description: FieldOptions mülk. Belge tarafından kullanılan şablonun dosya adını alır veya ayarlar.
type: docs
weight: 190
url: /tr/net/aspose.words.fields/fieldoptions/templatename/
---
## FieldOptions.TemplateName property

Belge tarafından kullanılan şablonun dosya adını alır veya ayarlar.

```csharp
public string TemplateName { get; set; }
```

### Notlar

Bu özellik şu kişi tarafından kullanılır:[`FieldTemplate`](../../fieldtemplate/) alan ise[`AttachedTemplate`](../../../aspose.words/document/attachedtemplate/) mülk boş.

Bu özellik boşsa varsayılan şablon dosyası adı`Normal.dotm` kullanıldı.

### Örnekler

Bir belgenin şablonunun yerel dosya sistemi konumunu görüntülemek için ŞABLON alanının nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Alanları kullanarak bir şablon adı belirleyebiliriz. Bu özellik "doc.AttachedTemplate" boş olduğunda kullanılır.
// Bu özellik boşsa, varsayılan şablon dosyası adı "Normal.dotm" kullanılır.
doc.FieldOptions.TemplateName = string.Empty;

FieldTemplate field = (FieldTemplate)builder.InsertField(FieldType.FieldTemplate, false);
Assert.AreEqual(" TEMPLATE ", field.GetFieldCode());

builder.Writeln();
field = (FieldTemplate)builder.InsertField(FieldType.FieldTemplate, false);
field.IncludeFullPath = true;

Assert.AreEqual(" TEMPLATE  \\p", field.GetFieldCode());

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.TEMPLATE.docx");
```

### Ayrıca bakınız

* class [FieldOptions](../)
* ad alanı [Aspose.Words.Fields](../../fieldoptions/)
* toplantı [Aspose.Words](../../../)


