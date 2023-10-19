---
title: Document.RenderToSize
linktitle: RenderToSize
articleTitle: RenderToSize
second_title: Aspose.Words for .NET
description: Document RenderToSize yöntem. Bir belge sayfasını birGraphics belirtilen boyuta nesne C#'da.
type: docs
weight: 690
url: /tr/net/aspose.words/document/rendertosize/
---
## Document.RenderToSize method

Bir belge sayfasını birGraphics belirtilen boyuta nesne.

```csharp
public float RenderToSize(int pageIndex, Graphics graphics, float x, float y, float width, 
    float height)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| pageIndex | Int32 | 0 tabanlı sayfa dizini. |
| graphics | Graphics | Oluşturulacak nesne. |
| x | Single | İşlenen sayfanın sol üst köşesinin X koordinatı (dünya birimleri cinsinden). |
| y | Single | İşlenen sayfanın sol üst köşesinin Y koordinatı (dünya birimleri cinsinden). |
| width | Single | İşlenen sayfanın kaplayabileceği maksimum genişlik (dünya birimleri cinsinden). |
| height | Single | Oluşturulan sayfanın kaplayabileceği maksimum yükseklik (dünya birimleri cinsinden). |

### Geri dönüş değeri

Oluşturulan sayfanın belirtilen boyuta sığması için otomatik olarak hesaplanan ölçek.

## Örnekler

Belgenin belirli bir konumda ve boyutta (.NetStandard 2.0) bit eşlem olarak nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

using (SKBitmap bitmap = new SKBitmap(700, 700))
{
    using (SKCanvas canvas = new SKCanvas(bitmap))
    {
        // Bu tuvali kullanarak oluşturacağımız sayfaya %70'lik bir ölçeklendirme faktörü uygulayın.
        canvas.Scale(70);

        // Sayfayı sayfanın üst ve sol kenarlarından 0,5" kaydır.
        canvas.Translate(0.5f, 0.5f);

        // Oluşturulan sayfayı 10 derece döndürün.
        canvas.RotateDegrees(10);

        // Bir dikdörtgen oluşturup çiziyoruz.
        SKRect rect = new SKRect(0f, 0f, 3f, 3f);
        canvas.DrawRect(rect, new SKPaint
        {
            Color = SKColors.Black,
            Style = SKPaintStyle.Stroke,
            StrokeWidth = 3f / 72f
        });

        // Belgenin ilk sayfasını yukarıdaki dikdörtgenle aynı boyuta getirin.
        // Dikdörtgen bu sayfayı çerçeveleyecektir.
        float returnedScale = doc.RenderToSize(0, canvas, 0f, 0f, 3f, 3f);

        Console.WriteLine("The image was rendered at {0:P0} zoom.", returnedScale);

        // Matrisi sıfırlayın ve ardından yeni bir ölçeklendirme ve çeviri kümesi uygulayın.
        canvas.ResetMatrix();
        canvas.Scale(5);
        canvas.Translate(10, 10);

        //Başka bir dikdörtgen oluştur.
        rect = new SKRect(0, 0, 50, 100);
        rect.Offset(90, 10);
        canvas.DrawRect(rect, new SKPaint
        {
            Color = SKColors.Black,
            Style = SKPaintStyle.Stroke,
            StrokeWidth = 1
        });

        // Yeni oluşturulan dikdörtgenin içindeki ilk sayfayı bir kez daha işleyin.
        doc.RenderToSize(0, canvas, 90, 10, 50, 100);

        using (SKFileWStream fs = new SKFileWStream(ArtifactsDir + "Rendering.RenderToSizeNetStandard2.png"))
        {
            bitmap.PeekPixels().Encode(fs, SKEncodedImageFormat.Png, 100);
        }
    }
}
```

Bir belgenin belirli bir konum ve boyutta bitmap'e nasıl dönüştürüleceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

using (Bitmap bmp = new Bitmap(700, 700))
{
    using (Graphics gr = Graphics.FromImage(bmp))
    {
        gr.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;

        // İnç değerini kullanmak için "PageUnit" özelliğini "GraphicsUnit.Inch" olarak ayarlayın
        // tanımlayacağımız her türlü dönüşüm ve boyut için ölçü birimi.
        gr.PageUnit = GraphicsUnit.Inch;

        // Çıkışı kenardan 0,5" kaydır.
        gr.TranslateTransform(0.5f, 0.5f);

        // Çıkışı 10 derece döndürün.
        gr.RotateTransform(10);

        // 3"x3" boyutunda bir dikdörtgen çizin.
        gr.DrawRectangle(new Pen(Color.Black, 3f / 72f), 0f, 0f, 3f, 3f);

        // Belgemizin ilk sayfasını dikdörtgenle aynı boyut ve dönüşümle çizin.
        // Dikdörtgen ilk sayfayı çerçeveleyecektir.
        float returnedScale = doc.RenderToSize(0, gr, 0f, 0f, 3f, 3f);

        // Bu, RenderToSize yönteminin belirtilen boyuta sığdırmak için ilk sayfaya uyguladığı ölçeklendirme faktörüdür.
        Assert.AreEqual(0.2566f, returnedScale, 0.0001f);

        // Milimetreyi veri birimi olarak kullanmak için "PageUnit" özelliğini "GraphicsUnit.Millimeter" olarak ayarlayın.
        // tanımlayacağımız her türlü dönüşüm ve boyut için ölçü birimi.
        gr.PageUnit = GraphicsUnit.Millimeter;

        // Önceki oluşturmada kullandığımız dönüşümleri sıfırlayın.
        gr.ResetTransform();

        // Başka bir dönüşüm kümesi uygulayın.
        gr.TranslateTransform(10, 10);
        gr.ScaleTransform(0.5f, 0.5f);
        gr.PageScale = 2f;

        // Başka bir dikdörtgen oluşturun ve bunu belgedeki başka bir sayfayı çerçevelemek için kullanın.
        gr.DrawRectangle(new Pen(Color.Black, 1), 90, 10, 50, 100);
        doc.RenderToSize(1, gr, 90, 10, 50, 100);

        bmp.Save(ArtifactsDir + "Rendering.RenderToSize.png");
    }
}
```

### Ayrıca bakınız

* class [Document](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
