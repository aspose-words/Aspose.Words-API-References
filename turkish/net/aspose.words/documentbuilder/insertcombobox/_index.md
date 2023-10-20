---
title: DocumentBuilder.InsertComboBox
linktitle: InsertComboBox
articleTitle: InsertComboBox
second_title: Aspose.Words for .NET
description: DocumentBuilder InsertComboBox yöntem. Geçerli konuma bir birleşik giriş kutusu form alanı ekler C#'da.
type: docs
weight: 300
url: /tr/net/aspose.words/documentbuilder/insertcombobox/
---
## DocumentBuilder.InsertComboBox method

Geçerli konuma bir birleşik giriş kutusu form alanı ekler.

```csharp
public FormField InsertComboBox(string name, string[] items, int selectedIndex)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| name | String | Form alanının adı. Boş bir dize olabilir. 20 karakterden uzun olan değer kesilecektir. |
| items | String[] | ComboBox'un öğeleri. Maksimum 25 öğedir. |
| selectedIndex | Int32 | ComboBox'ta seçilen öğenin dizini. |

### Geri dönüş değeri

Yeni eklenen form alanı düğümü.

## Notlar

Form alanı için bir ad belirlerseniz aynı adla otomatik olarak bir yer imi oluşturulur.

## Örnekler

Bir belgeye birleşik giriş kutusu form alanının nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Kullanıcının menüdeki öğelerden birini seçmesini isteyen bir form ekleyin.
builder.Write("Pick a fruit: ");
string[] items = { "Apple", "Banana", "Cherry" };
builder.InsertComboBox("DropDown", items, 0);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertComboBox.docx");
```

Form alanlarının nasıl oluşturulacağını gösterir.

```csharp
DocumentBuilder builder = new DocumentBuilder();

// Form alanları, belgedeki, kullanıcının değer girmesi istenerek etkileşimde bulunabileceği nesnelerdir.
// Bunları bir belge oluşturucu kullanarak oluşturabiliriz ve aşağıda bunu yapmanın iki yolu vardır.
// 1 - Temel metin girişi:
builder.InsertTextInput("My text input", TextFormFieldType.Regular, 
    "", "Enter your name here", 30);

// 2 - Bilgi istemi metnini ve bir dizi olası değeri içeren birleşik giriş kutusu:
string[] items =
{
    "-- Select your favorite footwear --", "Sneakers", "Oxfords", "Flip-flops", "Other"
};

builder.InsertParagraph();
builder.InsertComboBox("My combo box", items, 0);

builder.Document.Save(ArtifactsDir + "DocumentBuilder.CreateForm.docx");
```

### Ayrıca bakınız

* class [FormField](../../../aspose.words.fields/formfield/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
