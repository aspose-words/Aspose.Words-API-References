---
title: Style.Name
linktitle: Name
articleTitle: Name
second_title: .NET için Aspose.Words
description: Stil Adı özelliğini keşfedin, gelişmiş tasarım esnekliği ve kullanıcı deneyimi için stillerinizi kolayca yönetin ve özelleştirin.
type: docs
weight: 130
url: /tr/net/aspose.words/style/name/
---
## Style.Name property

Stilin adını alır veya ayarlar.

```csharp
public string Name { get; set; }
```

## Notlar

Boş dize olamaz.

Koleksiyonda zaten böyle bir isme sahip bir stil varsa, bu stil onu geçersiz kılacaktır. Etkilenen tüm düğümler yeni stile başvuracaktır.

## Örnekler

Bir belgenin stil koleksiyonuna nasıl erişileceğini gösterir.

```csharp
Document doc = new Document();

Assert.AreEqual(4, doc.Styles.Count);

// Aspose.Words kullanılarak oluşturulan bir belgenin varsayılan olarak içerdiği tüm stilleri sayın ve listeleyin.
using (IEnumerator<Style> stylesEnum = doc.Styles.GetEnumerator())
{
    while (stylesEnum.MoveNext())
    {
        Style curStyle = stylesEnum.Current;
        Console.WriteLine($"Style name:\t\"{curStyle.Name}\", of type \"{curStyle.Type}\"");
        Console.WriteLine($"\tSubsequent style:\t{curStyle.NextParagraphStyleName}");
        Console.WriteLine($"\tIs heading:\t\t\t{curStyle.IsHeading}");
        Console.WriteLine($"\tIs QuickStyle:\t\t{curStyle.IsQuickStyle}");

        Assert.AreEqual(doc, curStyle.Document);
    }
}
```

Bir belgenin stilinin nasıl kopyalanacağını gösterir.

```csharp
Document doc = new Document();

// AddCopy yöntemi belirtilen stilin bir kopyasını oluşturur ve
// stil için otomatik olarak "Başlık 1_0" gibi yeni bir ad üretir.
Style newStyle = doc.Styles.AddCopy(doc.Styles["Heading 1"]);

// Stilin tanımlayıcı adını değiştirmek için stilin "Ad" özelliğini kullanın.
newStyle.Name = "My Heading 1";

// Belgemiz artık farklı isimlere sahip, aynı görünümlü iki stile sahip.
// Stillerden birinin ayarlarını değiştirmek diğerini etkilemez.
newStyle.Font.Color = Color.Red;

Assert.AreEqual("My Heading 1", newStyle.Name);
Assert.AreEqual("Heading 1", doc.Styles["Heading 1"].Name);

Assert.AreEqual(doc.Styles["Heading 1"].Type, newStyle.Type);
Assert.AreEqual(doc.Styles["Heading 1"].Font.Name, newStyle.Font.Name);
Assert.AreEqual(doc.Styles["Heading 1"].Font.Size, newStyle.Font.Size);
Assert.AreNotEqual(doc.Styles["Heading 1"].Font.Color, newStyle.Font.Color);
```

### Ayrıca bakınız

* class [Style](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
