---
title: InsertComboBox
second_title: Aspose.Words for .NET API Referansı
description: Geçerli konuma bir birleşik giriş formu alanı ekler.
type: docs
weight: 280
url: /tr/net/aspose.words/documentbuilder/insertcombobox/
---
## DocumentBuilder.InsertComboBox method

Geçerli konuma bir birleşik giriş formu alanı ekler.

```csharp
public FormField InsertComboBox(string name, string[] items, int selectedIndex)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| name | String | Form alanının adı. Boş bir dize olabilir. 20 karakterden uzun olan değer kesilecektir. |
| items | String[] | ComboBox'ın öğeleri. Maksimum 25 adettir. |
| selectedIndex | Int32 | ComboBox'ta seçilen öğenin dizini. |

### Geri dönüş değeri

Yeni eklenen form alanı düğümü.

### Notlar

Form alanı için bir ad belirtirseniz, aynı ada sahip bir yer imi otomatik olarak oluşturulur.

### Örnekler

Bir belgeye birleşik giriş kutusu form alanının nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Kullanıcının menüden öğelerden birini seçmesini isteyen bir form ekleyin.
builder.Write("Pick a fruit: ");
string[] items = { "Apple", "Banana", "Cherry" };
builder.InsertComboBox("DropDown", items, 0);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertComboBox.docx");
```

Form alanlarının nasıl oluşturulacağını gösterir.

```csharp
DocumentBuilder builder = new DocumentBuilder();

// Form alanları, kullanıcıdan değerleri girmesi istenerek etkileşimde bulunabileceği belgedeki nesnelerdir.
// Bunları bir belge oluşturucu kullanarak oluşturabiliriz ve aşağıda bunu yapmanın iki yolu vardır.
// 1 - Temel metin girişi:
builder.InsertTextInput("My text input", TextFormFieldType.Regular, 
    "", "Enter your name here", 30);

// 2 - Komut istemi metni ve bir dizi olası değer içeren birleşik giriş kutusu:
string[] items =
{
    "-- Select your favorite footwear --", "Sneakers", "Oxfords", "Flip-flops", "Other"
};

builder.InsertParagraph();
builder.InsertComboBox("My combo box", items, 0);

builder.Document.Save(ArtifactsDir + "DocumentBuilder.CreateForm.docx");
```

### Ayrıca bakınız

* class [FormField](../../../aspose.words.fields/formfield)
* class [DocumentBuilder](../../documentbuilder)
* ad alanı [Aspose.Words](../../documentbuilder)
* toplantı [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->