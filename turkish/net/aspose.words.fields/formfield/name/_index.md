---
title: Name
second_title: Aspose.Words for .NET API Referansı
description: Form alanı adını alır veya ayarlar.
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

Birleşik giriş kutusunun nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Please select a fruit: ");

// Kullanıcının bir dizi diziden bir seçenek seçmesine izin verecek bir birleşik giriş kutusu ekleyin.
FormField comboBox = builder.InsertComboBox("MyComboBox", new[] { "Apple", "Banana", "Cherry" }, 0);

Assert.AreEqual("MyComboBox", comboBox.Name);
Assert.AreEqual(FieldType.FieldFormDropDown, comboBox.Type);
Assert.AreEqual("Apple", comboBox.Result);

// Form alanı bir "select" html etiketi şeklinde görünecektir.
doc.Save(ArtifactsDir + "FormFields.Create.html");
```

### Ayrıca bakınız

* class [FormField](../../formfield)
* ad alanı [Aspose.Words.Fields](../../formfield)
* toplantı [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
