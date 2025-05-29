---
title: FormField.Result
linktitle: Result
articleTitle: Result
second_title: .NET için Aspose.Words
description: FormField Result özelliğini keşfedin, form alanlarınızın dize çıktısını kolayca yönetin ve özelleştirin; böylece kullanıcı deneyiminizi geliştirin.
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

Metin form alanı için sonuç, alandaki metindir.

Bir onay kutusu form alanı için sonuç, işaretli veya işaretsiz olduğunu belirtmek üzere "1" veya "0" olabilir.

Açılır form alanı için sonuç, açılır listede seçilen dizedir.

Ayar`Result` bir metin form alanı için belirtilen format metni uygulanmaz[`TextInputFormat`](../textinputformat/) . Bir değer belirlemek ve the biçimini uygulamak istiyorsanız, şunu kullanın:[`SetTextInputValue`](../settextinputvalue/) yöntem.

Bir metin form alanı için[`TextInputDefault`](../textinputdefault/) değer uygulanırsa *value* dır`hükümsüz`.

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
