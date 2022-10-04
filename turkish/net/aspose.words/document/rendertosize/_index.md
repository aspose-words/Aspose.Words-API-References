---
title: RenderToSize
second_title: Aspose.Words for .NET API Referansı
description: Bir belge sayfasını birGraphics belirtilen bir boyuta nesne.
type: docs
weight: 670
url: /tr/net/aspose.words/document/rendertosize/
---
## Document.RenderToSize method

Bir belge sayfasını birGraphics belirtilen bir boyuta nesne.

```csharp
public float RenderToSize(int pageIndex, Graphics graphics, float x, float y, float width, 
    float height)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| pageIndex | Int32 | 0 tabanlı sayfa dizini. |
| graphics | Graphics | Oluşturulacak nesne. |
| x | Single | Oluşturulan sayfanın sol üst köşesinin X koordinatı (dünya birimleri cinsinden). |
| y | Single | Oluşturulan sayfanın sol üst köşesinin Y koordinatı (dünya birimleri cinsinden). |
| width | Single | Oluşturulan sayfanın kaplayabileceği maksimum genişlik (dünya birimleri cinsinden). |
| height | Single | Oluşturulan sayfanın kaplayabileceği maksimum yükseklik (dünya birimleri cinsinden). |

### Geri dönüş değeri

Oluşturulan sayfanın belirtilen boyuta sığması için otomatik olarak hesaplanan ölçek.

### Örnekler

Belgenin belirli bir konum ve boyutta (.NetStandard 2.0) bit eşlem olarak nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

using (SKBitmap bitmap = new SKBitmap(700, 700))
{
    using (SKCanvas canvas = new SKCanvas(bitmap))
    {
        // Bu tuvali kullanarak oluşturacağımız sayfaya %70'lik bir ölçekleme faktörü uygulayın.
        canvas.Scale(70);

        // Sayfayı, sayfanın üst ve sol kenarlarından 0,5" ötele.
        canvas.Translate(0.5f, 0.5f);

        // Oluşturulan sayfayı 10 derece döndür.
        canvas.RotateDegrees(10);

        // Bir dikdörtgen oluşturun ve çizin.
        SKRect rect = new SKRect(0f, 0f, 3f, 3f);
        canvas.DrawRect(rect, new SKPaint
        {
            Color = SKColors.Black,
            Style = SKPaintStyle.Stroke,
            StrokeWidth = 3f / 72f
        });

        // Belgenin ilk sayfasını yukarıdaki dikdörtgenle aynı boyutta işleyin.
        // Dikdörtgen bu sayfayı çerçeveleyecektir.
        float returnedScale = doc.RenderToSize(0, canvas, 0f, 0f, 3f, 3f);

        Console.WriteLine("The image was rendered at {0:P0} zoom.", returnedScale);

        // Matrisi sıfırlayın ve ardından yeni bir ölçekleme ve çeviri kümesi uygulayın.
        canvas.ResetMatrix();
        canvas.Scale(5);
        canvas.Translate(10, 10);

        // Başka bir dikdörtgen oluşturun.
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

Belgenin belirli bir konum ve boyutta bir bitmap olarak nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

using (Bitmap bmp = new Bitmap(700, 700))
{
    using (Graphics gr = Graphics.FromImage(bmp))
    {
        gr.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;

        // inç olarak kullanmak için "PageUnit" özelliğini "GraphicsUnit.Inch" olarak ayarlayın.
        // tanımlayacağımız herhangi bir dönüşüm ve boyut için ölçüm birimi.
        gr.PageUnit = GraphicsUnit.Inch;

        // Çıktı 0,5" kenardan ofset.
        gr.TranslateTransform(0.5f, 0.5f);

        // Çıktıyı 10 derece döndür.
        gr.RotateTransform(10);

        // 3"x3" bir dikdörtgen çizin.
        gr.DrawRectangle(new Pen(Color.Black, 3f / 72f), 0f, 0f, 3f, 3f);

        // Belgemizin ilk sayfasını dikdörtgenle aynı boyut ve dönüşümle çizelim.
        // Dikdörtgen ilk sayfayı çerçeveleyecektir.
        float returnedScale = doc.RenderToSize(0, gr, 0f, 0f, 3f, 3f);

        // Bu, RenderToSize yönteminin belirtilen boyuta sığdırmak için ilk sayfaya uyguladığı ölçeklendirme faktörüdür.
        Assert.AreEqual(0.2566f, returnedScale, 0.0001f);

        // Milimetre olarak kullanmak için "PageUnit" özelliğini "GraphicsUnit.Millimeter" olarak ayarlayın.
        // tanımlayacağımız herhangi bir dönüşüm ve boyut için ölçüm birimi.
        gr.PageUnit = GraphicsUnit.Millimeter;

        // Bir önceki işlemede kullandığımız dönüşümleri sıfırlayın.
        gr.ResetTransform();

         // Başka bir dönüşüm kümesi uygulayın.
        gr.TranslateTransform(10, 10);
        gr.ScaleTransform(0.5f, 0.5f);
        gr.PageScale = 2f;

        // Başka bir dikdörtgen oluşturun ve belgeden başka bir sayfayı çerçevelemek için kullanın.
        gr.DrawRectangle(new Pen(Color.Black, 1), 90, 10, 50, 100);
        doc.RenderToSize(1, gr, 90, 10, 50, 100);

        bmp.Save(ArtifactsDir + "Rendering.RenderToSize.png");
    }
}
```

### Ayrıca bakınız

* class [Document](../)
* ad alanı [Aspose.Words](../../document/)
* toplantı [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
