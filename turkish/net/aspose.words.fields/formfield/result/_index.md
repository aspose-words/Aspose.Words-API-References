---
title: FormField.Result
linktitle: Result
articleTitle: Result
second_title: Aspose.Words for .NET
description: FormField Result mülk. Bu form alanının sonucunu temsil eden bir dize alır veya ayarlar C#'da.
type: docs
weight: 170
url: /tr/net/aspose.words.fields/formfield/result/
---
## FormField.Result property

Bu form alanının sonucunu temsil eden bir dize alır veya ayarlar.

```csharp
public string Result { get; set; }
```

## Notlar

Bir metin formu alanı için sonuç, alandaki metindir.

Onay kutusu form alanı için sonuç, işaretli veya işaretsiz olduğunu belirtmek üzere "1" veya "0" olabilir.

Açılır form alanı için sonuç, açılır menüde seçilen dizedir.

Ayar`Result` bir metin formu alanı için şu şekilde belirtilen metin formatı geçerli değildir:[`TextInputFormat`](../textinputformat/) . Bir değer ayarlamak ve the biçimini uygulamak istiyorsanız[`SetTextInputValue`](../settextinputvalue/) yöntem.

Bir metin formu alanı için[`TextInputDefault`](../textinputdefault/) değer uygulanır eğer*value* dır-dir`hükümsüz`.

## Örnekler

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
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)
