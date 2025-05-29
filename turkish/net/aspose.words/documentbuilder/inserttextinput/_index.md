---
title: DocumentBuilder.InsertTextInput
linktitle: InsertTextInput
articleTitle: InsertTextInput
second_title: .NET için Aspose.Words
description: DocumentBuilder InsertTextInput yöntemi ile zahmetsizce metin form alanları ekleyin. Belgenizin etkileşimini ve kullanıcı deneyimini bugün geliştirin!
type: docs
weight: 510
url: /tr/net/aspose.words/documentbuilder/inserttextinput/
---
## DocumentBuilder.InsertTextInput method

Geçerli konuma bir metin formu alanı ekler.

```csharp
public FormField InsertTextInput(string name, TextFormFieldType type, string format, 
    string fieldValue, int maxLength)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| name | String | Form alanının adı. Boş bir dize olabilir. |
| type | TextFormFieldType | Metin form alanının türünü belirtir. |
| format | String | Form alanının değerini biçimlendirmek için kullanılan biçim dizesi. |
| fieldValue | String | Alanda gösterilecek metin. |
| maxLength | Int32 | Kullanıcının form alanına girebileceği maksimum uzunluk. Sınırsız uzunluk için sıfıra ayarlayın. |

### Geri dönüş değeri

Az önce eklenen form alanı düğümü.

## Notlar

Form alanı için bir ad belirttiğinizde, aynı adla otomatik olarak bir yer imi oluşturulur.

## Örnekler

Bir belgeye metin girişi form alanının nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Kullanıcıdan metin girmesini isteyen bir form ekleyin.
builder.InsertTextInput("TextInput", TextFormFieldType.Regular, "", "Enter your text here", 0);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertTextInput.docx");
```

Metin giriş formu alanının nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Please enter text here: ");

// Kullanıcının üzerine tıklayıp metin girmesine olanak verecek bir metin giriş alanı ekleyin.
// Kullanıcının üzerine yazabileceği ve iletebileceği bazı yer tutucu metinler atayın
// Form alanının içeriğinde herhangi bir sınır olmaması için maksimum metin uzunluğu 0'dır.
builder.InsertTextInput("TextInput1", TextFormFieldType.Regular, "", "Placeholder text", 0);

// Form alanı "input" html etiketi şeklinde, "text" türünde görünecektir.
doc.Save(ArtifactsDir + "FormFields.TextInput.html");
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
* enum [TextFormFieldType](../../../aspose.words.fields/textformfieldtype/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
