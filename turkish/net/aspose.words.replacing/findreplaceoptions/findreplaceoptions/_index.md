---
title: FindReplaceOptions
linktitle: FindReplaceOptions
articleTitle: FindReplaceOptions
second_title: .NET için Aspose.Words
description: Varsayılan ayarlarla yeni bir örneği kolayca başlatmak, arama ve değiştirme işlevselliğinizi geliştirmek için FindReplaceOptions oluşturucusunu keşfedin.
type: docs
weight: 10
url: /tr/net/aspose.words.replacing/findreplaceoptions/findreplaceoptions/
---
## FindReplaceOptions() {#constructor}

FindReplaceOptions sınıfının yeni bir örneğini varsayılan ayarlarla başlatır.

```csharp
public FindReplaceOptions()
```

## Örnekler

Yer değiştirme kalıpları içindeki yer değiştirmelerin nasıl tanınacağını ve kullanılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Jason gave money to Paul.");

Regex regex = new Regex(@"([A-z]+) gave money to ([A-z]+)");

FindReplaceOptions options = new FindReplaceOptions();
options.UseSubstitutions = true;

// Eski modu kullanmak pek çok gelişmiş özelliği desteklemez, bu yüzden bunu 'false' olarak ayarlamamız gerekir.
options.LegacyMode = false;

doc.Range.Replace(regex, @"$2 took money from $1", options);

Assert.AreEqual(doc.GetText(), "Paul took money from Jason.\f");
```

### Ayrıca bakınız

* class [FindReplaceOptions](../)
* ad alanı [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* toplantı [Aspose.Words](../../../)

---

## FindReplaceOptions(*[FindReplaceDirection](../../findreplacedirection/)*) {#constructor_1}

Belirtilen yönde FindReplaceOptions sınıfının yeni bir örneğini başlatır.

```csharp
public FindReplaceOptions(FindReplaceDirection direction)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| direction | FindReplaceDirection | Bul ve değiştir işleminin yönü. |

### Ayrıca bakınız

* enum [FindReplaceDirection](../../findreplacedirection/)
* class [FindReplaceOptions](../)
* ad alanı [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* toplantı [Aspose.Words](../../../)

---

## FindReplaceOptions(*[IReplacingCallback](../../ireplacingcallback/)*) {#constructor_3}

Belirtilen değiştirme geri aramasıyla FindReplaceOptions sınıfının yeni bir örneğini başlatır.

```csharp
public FindReplaceOptions(IReplacingCallback replacingCallback)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| replacingCallback | IReplacingCallback | Bulunan metni değiştirmek için kullanılacak geri çağırma. |

## Örnekler

Bir metin değiştirme işleminin düğümleri hangi sırayla geçtiğinin nasıl izleneceğini gösterir.

```csharp
public void Order(bool differentFirstPageHeaderFooter)
{
    Document doc = new Document(MyDir + "Header and footer types.docx");

    Section firstPageSection = doc.FirstSection;

    ReplaceLog logger = new ReplaceLog();
    FindReplaceOptions options = new FindReplaceOptions(logger);

    // İlk sayfa için farklı bir üstbilgi/altbilgi kullanılması arama sırasını etkileyecektir.
    firstPageSection.PageSetup.DifferentFirstPageHeaderFooter = differentFirstPageHeaderFooter;
    doc.Range.Replace(new Regex("(header|footer)"), "", options);

    if (differentFirstPageHeaderFooter)
        Assert.AreEqual("First header\nFirst footer\nSecond header\nSecond footer\nThird header\nThird footer\n", 
            logger.Text.Replace("\r", ""));
    else
        Assert.AreEqual("Third header\nFirst header\nThird footer\nFirst footer\nSecond header\nSecond footer\n", 
            logger.Text.Replace("\r", ""));
}

/// <summary>
/// Bir bul-değiştir işlemi sırasında, işlemin 'bulduğu' metni içeren her düğümün içeriğini kaydeder,
/// değiştirme gerçekleşmeden önceki hali.
/// Bu, metin değiştirme işleminin düğümleri hangi sırayla dolaşacağını görüntüler.
/// </summary>
private class ReplaceLog : IReplacingCallback
{
    public ReplaceAction Replacing(ReplacingArgs args)
    {
        mTextBuilder.AppendLine(args.MatchNode.GetText());
        return ReplaceAction.Skip;
    }

    internal string Text => mTextBuilder.ToString();

    private readonly StringBuilder mTextBuilder = new StringBuilder();
}
```

### Ayrıca bakınız

* interface [IReplacingCallback](../../ireplacingcallback/)
* class [FindReplaceOptions](../)
* ad alanı [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* toplantı [Aspose.Words](../../../)

---

## FindReplaceOptions(*[FindReplaceDirection](../../findreplacedirection/), [IReplacingCallback](../../ireplacingcallback/)*) {#constructor_2}

Belirtilen yön ve geri aramayı değiştirerek FindReplaceOptions sınıfının yeni bir örneğini başlatır.

```csharp
public FindReplaceOptions(FindReplaceDirection direction, IReplacingCallback replacingCallback)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| direction | FindReplaceDirection | Bul ve değiştir işleminin yönü. |
| replacingCallback | IReplacingCallback | Bulunan metni değiştirmek için kullanılacak geri çağırma. |

### Ayrıca bakınız

* enum [FindReplaceDirection](../../findreplacedirection/)
* interface [IReplacingCallback](../../ireplacingcallback/)
* class [FindReplaceOptions](../)
* ad alanı [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* toplantı [Aspose.Words](../../../)
