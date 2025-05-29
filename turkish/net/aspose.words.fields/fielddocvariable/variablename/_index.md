---
title: FieldDocVariable.VariableName
linktitle: VariableName
articleTitle: VariableName
second_title: .NET için Aspose.Words
description: Belge değişkenlerini kolayca yönetmek için FieldDocVariable VariableName özelliğini keşfedin. Bugün belge yönetiminizi basitleştirin ve iyileştirin!
type: docs
weight: 20
url: /tr/net/aspose.words.fields/fielddocvariable/variablename/
---
## FieldDocVariable.VariableName property

Alınacak belge değişkeninin adını alır veya ayarlar.

```csharp
public string VariableName { get; set; }
```

## Örnekler

Belge özelliklerini ve değişkenlerini görüntülemek için DOCPROPERTY alanlarının nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Aşağıda DOCPROPERTY alanlarının iki kullanım şekli bulunmaktadır.
// 1 - Yerleşik bir özelliği görüntüle:
// "Kategori" yerleşik özelliği için özel bir değer ayarlayın, ardından buna başvuran bir DOCPROPERTY alanı ekleyin.
doc.BuiltInDocumentProperties.Category = "My category";

FieldDocProperty fieldDocProperty = (FieldDocProperty)builder.InsertField(" DOCPROPERTY Category ");
fieldDocProperty.Update();

Assert.AreEqual(" DOCPROPERTY Category ", fieldDocProperty.GetFieldCode());
Assert.AreEqual("My category", fieldDocProperty.Result);

builder.InsertParagraph();

// 2 - Özel bir belge değişkenini görüntüle:
// Özel bir değişken tanımlayın, ardından bu değişkene DOCPROPERTY alanıyla başvurun.
Assert.AreEqual(0, doc.Variables.Count);
doc.Variables.Add("My variable", "My variable's value");

FieldDocVariable fieldDocVariable = (FieldDocVariable)builder.InsertField(FieldType.FieldDocVariable, true);
fieldDocVariable.VariableName = "My Variable";
fieldDocVariable.Update();

Assert.AreEqual(" DOCVARIABLE  \"My Variable\"", fieldDocVariable.GetFieldCode());
Assert.AreEqual("My variable's value", fieldDocVariable.Result);

doc.Save(ArtifactsDir + "Field.DOCPROPERTY.DOCVARIABLE.docx");
```

### Ayrıca bakınız

* class [FieldDocVariable](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)
