---
title: FieldOptions.TemplateName
linktitle: TemplateName
articleTitle: TemplateName
second_title: .NET için Aspose.Words
description: Gelişmiş organizasyon ve verimlilik için belgenizin şablon dosya adını kolayca yönetmek üzere FieldOptions TemplateName özelliğini keşfedin.
type: docs
weight: 190
url: /tr/net/aspose.words.fields/fieldoptions/templatename/
---
## FieldOptions.TemplateName property

Belge tarafından kullanılan şablonun dosya adını alır veya ayarlar.

```csharp
public string TemplateName { get; set; }
```

## Notlar

Bu özellik tarafından kullanılıyor[`FieldTemplate`](../../fieldtemplate/) alan eğer[`AttachedTemplate`](../../../aspose.words/document/attachedtemplate/) mülk boş.

Bu özellik boşsa, varsayılan şablon dosya adı`Normal.nokta` kullanılır.

## Örnekler

Bir belgenin şablonunun yerel dosya sistemi konumunu görüntülemek için ŞABLON alanının nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Alanları kullanarak bir şablon adı belirleyebiliriz. Bu özellik "doc.AttachedTemplate" boş olduğunda kullanılır.
// Bu özellik boşsa varsayılan şablon dosya adı "Normal.dotm" kullanılır.
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
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)
