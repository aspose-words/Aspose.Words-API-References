---
title: FormField.Type
linktitle: Type
articleTitle: Type
second_title: .NET için Aspose.Words
description: Web formlarınızın işlevselliğini ve kullanıcı deneyimini geliştirmek için çeşitli form alanı türlerini kolayca tanımlayıp kullanmak amacıyla FormField Type özelliğini keşfedin.
type: docs
weight: 220
url: /tr/net/aspose.words.fields/formfield/type/
---
## FormField.Type property

Form alan türünü döndürür.

```csharp
public FieldType Type { get; }
```

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

* enum [FieldType](../../fieldtype/)
* class [FormField](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)
