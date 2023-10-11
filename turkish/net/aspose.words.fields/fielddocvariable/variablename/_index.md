---
title: FieldDocVariable.VariableName
second_title: Aspose.Words for .NET API Referansı
description: FieldDocVariable mülk. Alınacak belge değişkeninin adını alır veya ayarlar.
type: docs
weight: 20
url: /tr/net/aspose.words.fields/fielddocvariable/variablename/
---
## FieldDocVariable.VariableName property

Alınacak belge değişkeninin adını alır veya ayarlar.

```csharp
public string VariableName { get; set; }
```

### Örnekler

Belge özelliklerini ve değişkenlerini görüntülemek için DOCPROPERTY alanlarının nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Aşağıda DOCPROPERTY alanlarını kullanmanın iki yolu verilmiştir.
// 1 - Yerleşik bir özelliği görüntüle:
// "Kategori" yerleşik özelliği için özel bir değer belirleyin, ardından buna referans veren bir DOCPROPERTY alanı ekleyin.
doc.BuiltInDocumentProperties.Category = "My category";

FieldDocProperty fieldDocProperty = (FieldDocProperty)builder.InsertField(" DOCPROPERTY Category ");
fieldDocProperty.Update();

Assert.AreEqual(" DOCPROPERTY Category ", fieldDocProperty.GetFieldCode());
Assert.AreEqual("My category", fieldDocProperty.Result);

builder.InsertParagraph();

// 2 - Özel bir belge değişkeni görüntüleyin:
// Özel bir değişken tanımlayın, ardından bu değişkene DOCPROPERTY alanıyla referans verin.
Assert.That(doc.Variables, Is.Empty);
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
* ad alanı [Aspose.Words.Fields](../../fielddocvariable/)
* toplantı [Aspose.Words](../../../)


