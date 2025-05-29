---
title: DocumentBuilder.InsertComboBox
linktitle: InsertComboBox
articleTitle: InsertComboBox
second_title: .NET için Aspose.Words
description: Belgelerinizi DocumentBuilder InsertComboBox yöntemiyle geliştirin. Geliştirilmiş kullanıcı deneyimi için etkileşimli birleşik kutu form alanlarını kolayca ekleyin.
type: docs
weight: 300
url: /tr/net/aspose.words/documentbuilder/insertcombobox/
---
## DocumentBuilder.InsertComboBox method

Geçerli konuma bir açılır kutu form alanı ekler.

```csharp
public FormField InsertComboBox(string name, string[] items, int selectedIndex)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| name | String | Form alanının adı. Boş bir dize olabilir. 20 karakterden uzun değer kesilecektir. |
| items | String[] | ComboBox'un öğeleri. Maksimum 25 öğe. |
| selectedIndex | Int32 | ComboBox'ta seçili öğenin dizini. |

### Geri dönüş değeri

Az önce eklenen form alanı düğümü.

## Notlar

Form alanı için bir ad belirttiğinizde, aynı adla otomatik olarak bir yer imi oluşturulur.

## Örnekler

Bir belgeye birleşik kutu form alanının nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Kullanıcının menüden bir öğeyi seçmesini isteyen bir form ekleyin.
builder.Write("Pick a fruit: ");
string[] items = { "Apple", "Banana", "Cherry" };
builder.InsertComboBox("DropDown", items, 0);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertComboBox.docx");
```

Form alanlarının nasıl oluşturulacağını gösterir.

```csharp
DocumentBuilder builder = new DocumentBuilder();

// Form alanları, kullanıcının değer girmesi istendiğinde etkileşime girebileceği belgedeki nesnelerdir.
// Bunları bir belge oluşturucu kullanarak oluşturabiliriz ve aşağıda bunu yapmanın iki yolu bulunmaktadır.
// 1 - Temel metin girişi:
builder.InsertTextInput("My text input", TextFormFieldType.Regular, 
    "", "Enter your name here", 30);

// 2 - İstem metni ve olası değer aralığı içeren birleşik kutu:
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
