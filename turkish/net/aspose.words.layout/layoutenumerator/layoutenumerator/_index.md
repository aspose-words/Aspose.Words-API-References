---
title: LayoutEnumerator
second_title: Aspose.Words for .NET API Referansı
description: Bu sınıfın yeni örneğini başlatır.
type: docs
weight: 10
url: /tr/net/aspose.words.layout/layoutenumerator/layoutenumerator/
---
## LayoutEnumerator constructor

Bu sınıfın yeni örneğini başlatır.

```csharp
public LayoutEnumerator(Document document)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| document | Document | Sayfa düzeni modeli numaralandırılacak bir belge. |

### Notlar

Belgenin sayfa yerleşim modeli oluşturulmamışsa numaralandırıcı çağırır[`UpdatePageLayout`](../../../aspose.words/document/updatepagelayout/) inşa etmek için.

Belge her güncellendiğinde ve yeni sayfa düzeni modeli oluşturulduğunda, ona erişmek için yeni bir numaralandırıcı kullanılmalıdır.

### Örnekler

Bir belgenin yerleşim varlıklarını geçmenin yollarını gösterir.

```csharp
public void LayoutEnumerator()
{
    // Çeşitli düzen varlıkları içeren bir belge açın.
    // Mizanpaj varlıkları, LayoutEntityType enum'a dahil edilen sayfalar, hücreler, satırlar, çizgiler ve diğer nesnelerdir.
    // Her yerleşim öğesinin belge gövdesinde kapladığı dikdörtgen bir alan vardır.
    Document doc = new Document(MyDir + "Layout entities.docx");

    // Bu varlıkları bir ağaç gibi dolaşabilen bir numaralandırıcı oluşturun.
    LayoutEnumerator layoutEnumerator = new LayoutEnumerator(doc);

    Assert.AreEqual(doc, layoutEnumerator.Document);

    layoutEnumerator.MoveParent(LayoutEntityType.Page);

    Assert.AreEqual(LayoutEntityType.Page, layoutEnumerator.Type);
    Assert.Throws<InvalidOperationException>(() => Console.WriteLine(layoutEnumerator.Text));

    // Numaralandırıcının ilk düzen varlığında olacağından emin olmak için bu yöntemi çağırabiliriz.
    layoutEnumerator.Reset();

    // Yerleşim numaralandırıcısının yerleşim varlıklarını nasıl geçeceğini belirleyen iki sipariş vardır.
    // birden çok sayfaya yayılan varlıklarla karşılaştığında.
    // 1 - Görsel sırayla:
    // Bir varlığın birden çok sayfaya yayılan alt öğeleri arasında gezinirken,
    // sayfa düzeni önceliklidir ve bu sayfadaki diğer alt öğelere geçeriz ve sonrakilerden kaçınırız.
    Console.WriteLine("Traversing from first to last, elements between pages separated:");
    TraverseLayoutForward(layoutEnumerator, 1);

    // Numaralandırıcımız artık koleksiyonun sonunda. Başa dönmek için yerleşim varlıklarını geriye doğru hareket ettirebiliriz.
    Console.WriteLine("Traversing from last to first, elements between pages separated:");
    TraverseLayoutBackward(layoutEnumerator, 1);

    // 2 - Mantıksal sırayla:
    // Bir varlığın birden çok sayfaya yayılan alt öğeleri arasında gezinirken,
    // numaralandırıcı, tüm alt varlıklar arasında geçiş yapmak için sayfalar arasında hareket edecektir.
    Console.WriteLine("Traversing from first to last, elements between pages mixed:");
    TraverseLayoutForwardLogical(layoutEnumerator, 1);

    Console.WriteLine("Traversing from last to first, elements between pages mixed:");
    TraverseLayoutBackwardLogical(layoutEnumerator, 1);
}

/// <summary>
/// layoutEnumerator'ın layout varlık koleksiyonunu önden arkaya numaralandırın,
/// önce derinlemesine ve "Görsel" sırayla.
/// </summary>
private static void TraverseLayoutForward(LayoutEnumerator layoutEnumerator, int depth)
{
    do
    {
        PrintCurrentEntity(layoutEnumerator, depth);

        if (layoutEnumerator.MoveFirstChild())
        {
            TraverseLayoutForward(layoutEnumerator, depth + 1);
            layoutEnumerator.MoveParent();
        }
    } while (layoutEnumerator.MoveNext());
}

/// <summary>
/// layoutEnumerator'ın düzen varlık koleksiyonunu arkadan öne doğru numaralandırın,
/// önce derinlemesine ve "Görsel" sırayla.
/// </summary>
private static void TraverseLayoutBackward(LayoutEnumerator layoutEnumerator, int depth)
{
    do
    {
        PrintCurrentEntity(layoutEnumerator, depth);

        if (layoutEnumerator.MoveLastChild())
        {
            TraverseLayoutBackward(layoutEnumerator, depth + 1);
            layoutEnumerator.MoveParent();
        }
    } while (layoutEnumerator.MovePrevious());
}

/// <summary>
/// layoutEnumerator'ın layout varlık koleksiyonunu önden arkaya numaralandırın,
/// önce derinlemesine ve "Mantıksal" sırayla.
/// </summary>
private static void TraverseLayoutForwardLogical(LayoutEnumerator layoutEnumerator, int depth)
{
    do
    {
        PrintCurrentEntity(layoutEnumerator, depth);

        if (layoutEnumerator.MoveFirstChild())
        {
            TraverseLayoutForwardLogical(layoutEnumerator, depth + 1);
            layoutEnumerator.MoveParent();
        }
    } while (layoutEnumerator.MoveNextLogical());
}

/// <summary>
/// layoutEnumerator'ın düzen varlık koleksiyonunu arkadan öne doğru numaralandırın,
/// önce derinlemesine ve "Mantıksal" sırayla.
/// </summary>
private static void TraverseLayoutBackwardLogical(LayoutEnumerator layoutEnumerator, int depth)
{
    do
    {
        PrintCurrentEntity(layoutEnumerator, depth);

        if (layoutEnumerator.MoveLastChild())
        {
            TraverseLayoutBackwardLogical(layoutEnumerator, depth + 1);
            layoutEnumerator.MoveParent();
        }
    } while (layoutEnumerator.MovePreviousLogical());
}

/// <summary>
/// Metni sekme karakterleriyle girintilerken layoutEnumerator'ın mevcut varlığı hakkındaki bilgileri konsola yazdırın
/// yapıcı LayoutEnumerator örneğinde sağladığımız kök düğüme göre derinliğine göre.
/// Sonda işlediğimiz dikdörtgen, varlığın belgede kapladığı alanı ve konumu temsil eder.
/// </summary>
private static void PrintCurrentEntity(LayoutEnumerator layoutEnumerator, int indent)
{
    string tabs = new string('\t', indent);

    Console.WriteLine(layoutEnumerator.Kind == string.Empty
        ? $"{tabs}-> Entity type: {layoutEnumerator.Type}"
        : $"{tabs}-> Entity type & kind: {layoutEnumerator.Type}, {layoutEnumerator.Kind}");

    // Yalnızca yayılma alanları metin içerebilir.
    if (layoutEnumerator.Type == LayoutEntityType.Span)
        Console.WriteLine($"{tabs}   Span contents: \"{layoutEnumerator.Text}\"");

    RectangleF leRect = layoutEnumerator.Rectangle;
    Console.WriteLine($"{tabs}   Rectangle dimensions {leRect.Width}x{leRect.Height}, X={leRect.X} Y={leRect.Y}");
    Console.WriteLine($"{tabs}   Page {layoutEnumerator.PageIndex}");
}
```

### Ayrıca bakınız

* class [Document](../../../aspose.words/document/)
* class [LayoutEnumerator](../)
* ad alanı [Aspose.Words.Layout](../../layoutenumerator/)
* toplantı [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
