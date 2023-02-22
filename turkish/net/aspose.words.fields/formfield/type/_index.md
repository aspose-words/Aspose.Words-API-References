---
title: FormField.Type
second_title: Aspose.Words for .NET API Referansı
description: FormField mülk. Form alanı türünü döndürür.
type: docs
weight: 220
url: /tr/net/aspose.words.fields/formfield/type/
---
## FormField.Type property

Form alanı türünü döndürür.

```csharp
public FieldType Type { get; }
```

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

* enum [FieldType](../../fieldtype/)
* class [FormField](../)
* ad alanı [Aspose.Words.Fields](../../formfield/)
* toplantı [Aspose.Words](../../../)


