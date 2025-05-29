---
title: FormField.Name
linktitle: Name
articleTitle: Name
second_title: .NET için Aspose.Words
description: Daha iyi kullanıcı etkileşimi ve veri toplama için formlarınızı özelleştirmek ve optimize etmek amacıyla FormField Name özelliğini nasıl kolayca yöneteceğinizi keşfedin.
type: docs
weight: 130
url: /tr/net/aspose.words.fields/formfield/name/
---
## FormField.Name property

Form alan adını alır veya ayarlar.

```csharp
public string Name { get; set; }
```

## Notlar

Microsoft Word en fazla 20 karakter uzunluğundaki dizelere izin verir.

## Örnekler

Bir açılır kutunun nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Please select a fruit: ");

// Kullanıcının bir dizi dize arasından bir seçenek seçmesine izin verecek bir açılır kutu ekleyin.
FormField comboBox = builder.InsertComboBox("MyComboBox", new[] { "Apple", "Banana", "Cherry" }, 0);

Assert.AreEqual("MyComboBox", comboBox.Name);
Assert.AreEqual(FieldType.FieldFormDropDown, comboBox.Type);
Assert.AreEqual("Apple", comboBox.Result);

// Form alanı "select" html etiketi biçiminde görünecektir.
doc.Save(ArtifactsDir + "FormFields.Create.html");
```

### Ayrıca bakınız

* class [FormField](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)
