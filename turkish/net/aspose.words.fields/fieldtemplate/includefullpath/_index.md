---
title: FieldTemplate.IncludeFullPath
linktitle: IncludeFullPath
articleTitle: IncludeFullPath
second_title: .NET için Aspose.Words
description: Projenizin verimliliğini ve organizasyonunu artırarak tam dosya yolu eklemeyi kolayca yönetmek için FieldTemplate IncludeFullPath özelliğini keşfedin.
type: docs
weight: 20
url: /tr/net/aspose.words.fields/fieldtemplate/includefullpath/
---
## FieldTemplate.IncludeFullPath property

Tam dosya yolu adının eklenip eklenmeyeceğini alır veya ayarlar.

```csharp
public bool IncludeFullPath { get; set; }
```

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

* class [FieldTemplate](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)
