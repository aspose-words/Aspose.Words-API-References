---
title: FindReplaceOptions.IgnoreFields
linktitle: IgnoreFields
articleTitle: IgnoreFields
second_title: .NET için Aspose.Words
description: Alanlar içindeki metni kolayca yönetmek için FindReplaceOptions IgnoreFields özelliğini keşfedin. Verimli arama için içeriği ne zaman yoksayacağınızı kontrol edin!
type: docs
weight: 80
url: /tr/net/aspose.words.replacing/findreplaceoptions/ignorefields/
---
## FindReplaceOptions.IgnoreFields property

Alanların içindeki metni yoksaymayı belirten bir Boole değeri alır veya ayarlar. Varsayılan değer`YANLIŞ` .

```csharp
public bool IgnoreFields { get; set; }
```

## Notlar

Bu seçenek tüm alanı etkiler ( arasındaki tüm düğümler)FieldStart VeFieldEnd).

Yalnızca alan kodlarını yoksaymak için lütfen ilgili seçeneği kullanın[`IgnoreFieldCodes`](../ignorefieldcodes/).

## Örnekler

Alanların içindeki metnin nasıl göz ardı edileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");
builder.InsertField("QUOTE", "Hello again!");

// Bul ve değiştir işlemini değiştirmek için "FindReplaceOptions" nesnesini kullanabiliriz.
FindReplaceOptions options = new FindReplaceOptions();

// Bul ve değiştir özelliğini elde etmek için "IgnoreFields" bayrağını "true" olarak ayarlayın
// alanların içindeki metni yok sayma işlemi.
// Bul ve değiştir özelliğini elde etmek için "IgnoreFields" bayrağını "false" olarak ayarlayın
// Alanların içindeki metinleri de arama işlemi.
options.IgnoreFields = ignoreTextInsideFields;

doc.Range.Replace("Hello", "Greetings", options);

Assert.AreEqual(
    ignoreTextInsideFields
        ? "Greetings world!\r\u0013QUOTE\u0014Hello again!\u0015"
        : "Greetings world!\r\u0013QUOTE\u0014Greetings again!\u0015", doc.GetText().Trim());
```

### Ayrıca bakınız

* class [FindReplaceOptions](../)
* ad alanı [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* toplantı [Aspose.Words](../../../)
