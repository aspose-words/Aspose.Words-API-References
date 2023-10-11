---
title: FormField.Name
second_title: Aspose.Words for .NET API Referansı
description: FormField mülk. Form alanı adını alır veya ayarlar.
type: docs
weight: 130
url: /tr/net/aspose.words.fields/formfield/name/
---
## FormField.Name property

Form alanı adını alır veya ayarlar.

```csharp
public string Name { get; set; }
```

### Notlar

Microsoft Word, en fazla 20 karakterden oluşan dizelere izin verir.

### Örnekler

Açılan kutunun nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Please select a fruit: ");

// Kullanıcının bir dizi dizeden bir seçenek seçmesine olanak tanıyacak bir açılan kutu ekleyin.
FormField comboBox = builder.InsertComboBox("MyComboBox", new[] { "Apple", "Banana", "Cherry" }, 0);

Assert.AreEqual("MyComboBox", comboBox.Name);
Assert.AreEqual(FieldType.FieldFormDropDown, comboBox.Type);
Assert.AreEqual("Apple", comboBox.Result);

// Form alanı "select" html etiketi şeklinde görünecektir.
doc.Save(ArtifactsDir + "FormFields.Create.html");
```

### Ayrıca bakınız

* class [FormField](../)
* ad alanı [Aspose.Words.Fields](../../formfield/)
* toplantı [Aspose.Words](../../../)


