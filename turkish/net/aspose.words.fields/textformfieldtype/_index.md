---
title: Enum TextFormFieldType
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Fields.TextFormFieldType Sıralama. Metin formu alanının türünü belirtir.
type: docs
weight: 2770
url: /tr/net/aspose.words.fields/textformfieldtype/
---
## TextFormFieldType enumeration

Metin formu alanının türünü belirtir.

```csharp
public enum TextFormFieldType
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Regular | `0` | Metin formu alanı herhangi bir metni içerebilir. |
| Number | `1` | Metin formu alanı yalnızca rakamlardan oluşabilir. |
| Date | `2` | Metin formu alanı yalnızca geçerli bir tarih değeri içerebilir. |
| CurrentDate | `3` | Metin formu alanı değeri, alanın güncellendiği geçerli tarihtir. |
| CurrentTime | `4` | Metin formu alanı değeri, alanın güncellendiği geçerli zamandır. |
| Calculated | `5` | Metin formu alanı değeri, 'de belirtilen ifadeden hesaplanır.[`TextInputDefault`](../formfield/textinputdefault/) özellik. |

### Örnekler

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

* ad alanı [Aspose.Words.Fields](../../aspose.words.fields/)
* toplantı [Aspose.Words](../../)


