---
title: TextFormFieldType Enum
linktitle: TextFormFieldType
articleTitle: TextFormFieldType
second_title: .NET için Aspose.Words
description: Gelişmiş belge otomasyonu ve özelleştirmesi için çeşitli metin formu alan türlerini tanımlayan Aspose.Words.Fields.TextFormFieldType enum'unu keşfedin.
type: docs
weight: 3180
url: /tr/net/aspose.words.fields/textformfieldtype/
---
## TextFormFieldType enumeration

Bir metin form alanının türünü belirtir.

```csharp
public enum TextFormFieldType
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Regular | `0` | Metin form alanı herhangi bir metni içerebilir. |
| Number | `1` | Metin form alanı yalnızca sayılar içerebilir. |
| Date | `2` | Metin form alanı yalnızca geçerli bir tarih değeri içerebilir. |
| CurrentDate | `3` | Metin form alanı değeri, alanın güncellendiği geçerli tarihtir. |
| CurrentTime | `4` | Metin form alanı değeri, alanın güncellendiği geçerli zamandır. |
| Calculated | `5` | Metin form alanı değeri, 'de belirtilen ifadeden hesaplanır.[`TextInputDefault`](../formfield/textinputdefault/) mülk. |

## Örnekler

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

* ad alanı [Aspose.Words.Fields](../../aspose.words.fields/)
* toplantı [Aspose.Words](../../)
