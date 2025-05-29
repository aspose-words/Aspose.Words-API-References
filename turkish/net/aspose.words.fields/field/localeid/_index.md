---
title: Field.LocaleId
linktitle: LocaleId
articleTitle: LocaleId
second_title: .NET için Aspose.Words
description: Alanınızın LocaleId özelliğini zahmetsizce yönetin. Uygulamalarınızda gelişmiş yerelleştirme ve kullanıcı deneyimi için LCID'yi alın veya ayarlayın.
type: docs
weight: 60
url: /tr/net/aspose.words.fields/field/localeid/
---
## Field.LocaleId property

Alanın LCID'sini alır veya ayarlar.

```csharp
public int LocaleId { get; set; }
```

## Örnekler

Bir alanın nasıl ekleneceğini ve yerel ayarlarıyla nasıl çalışılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Bir TARİH alanı ekleyin ve ardından gösterilecek tarihi yazdırın.
// Konunuzun güncel kültürü, tarihin biçimini belirler.
Field field = builder.InsertField(@"DATE");
Console.WriteLine($"Today's date, as displayed in the \"{CultureInfo.CurrentCulture.EnglishName}\" culture: {field.Result}");

Assert.AreEqual(1033, field.LocaleId);
// Konumuzun kültürünü değiştirmek DATE alanının sonucunu etkileyecektir.
// DATE alanının farklı bir kültürdeki tarihi göstermesini sağlamanın bir başka yolu da LocaleId özelliğini kullanmaktır.
// Bu şekilde bu etkiyi elde etmek için thread'in kültürünü değiştirmek zorunda kalmayız.
doc.FieldOptions.FieldUpdateCultureSource = FieldUpdateCultureSource.FieldCode;
CultureInfo de = new CultureInfo("de-DE");
field.LocaleId = de.LCID;
field.Update();

Console.WriteLine($"Today's date, as displayed according to the \"{CultureInfo.GetCultureInfo(field.LocaleId).EnglishName}\" culture: {field.Result}");
```

### Ayrıca bakınız

* class [Field](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)
