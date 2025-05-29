---
title: Style.BuiltIn
linktitle: BuiltIn
articleTitle: BuiltIn
second_title: .NET için Aspose.Words
description: Bir stilin MS Word'de yerleşik bir seçenek olup olmadığını keşfedin. Word'ün yerleşik stillerine ilişkin kapsamlı kılavuzumuzla belge tasarımınızı geliştirin!
type: docs
weight: 40
url: /tr/net/aspose.words/style/builtin/
---
## Style.BuiltIn property

Bu stil MS Word'deki yerleşik stillerden biriyse doğrudur.

```csharp
public bool BuiltIn { get; }
```

## Örnekler

Özel stilleri yerleşik stillerden nasıl ayırt edeceğinizi gösterir.

```csharp
Document doc = new Document();

// Microsoft Word kullanarak veya Aspose.Words'ü programlı olarak kullanarak bir belge oluşturduğumuzda,
// Belge, görünümünü değiştirmek için metne uygulanacak bir dizi stil ile birlikte gelecektir.
// Bu yerleşik stillere, belgenin "Stiller" koleksiyonu aracılığıyla erişebiliriz.
// Bu stillerin hepsinde "BuiltIn" bayrağı "true" olarak ayarlanacaktır.
Style style = doc.Styles["Emphasis"];

Assert.True(style.BuiltIn);

// Özel bir stil oluşturup koleksiyona ekleyin.
 // Bu tür özel stiller için "Yerleşik" bayrağı "yanlış" olarak ayarlanacaktır.
style = doc.Styles.Add(StyleType.Character, "MyStyle");
style.Font.Color = Color.Navy;
style.Font.Name = "Courier New";

Assert.False(style.BuiltIn);
```

### Ayrıca bakınız

* class [Style](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
