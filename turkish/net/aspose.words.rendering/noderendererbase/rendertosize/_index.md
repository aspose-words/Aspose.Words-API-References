---
title: NodeRendererBase.RenderToSize
linktitle: RenderToSize
articleTitle: RenderToSize
second_title: .NET için Aspose.Words
description: Geliştirilmiş görsel çıktı için şekilleri istediğiniz boyutta Grafik nesnelerine verimli bir şekilde dönüştürmek üzere NodeRendererBase RenderToSize yöntemini keşfedin.
type: docs
weight: 80
url: /tr/net/aspose.words.rendering/noderendererbase/rendertosize/
---
## NodeRendererBase.RenderToSize method

Şekli birGraphics nesnesini belirtilen bir boyuta ayarlayın.

```csharp
public float RenderToSize(Graphics graphics, float x, float y, float width, float height)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| graphics | Graphics | Hangi nesneye render yapılacağı. |
| x | Single | İşlenen şeklin sol üst köşesinin X koordinatı (dünya birimleri cinsinden). |
| y | Single | İşlenen şeklin sol üst köşesinin Y koordinatı (dünya birimleri cinsinden). |
| width | Single | İşlenen şeklin kaplayabileceği maksimum genişlik (dünya birimi cinsinden). |
| height | Single | Oluşturulan şeklin kaplayabileceği maksimum yükseklik (dünya birimi cinsinden). |

### Geri dönüş değeri

İşlenen şeklin belirtilen boyuta uyması için otomatik olarak hesaplanan ölçek.

## Örnekler

Bir şeklin Graphics nesnesiyle nasıl işleneceğini ve Windows Form kullanılarak nasıl görüntüleneceğini gösterir.

```csharp
public void RenderShapesOnForm()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    ShapeForm shapeForm = new ShapeForm(new Size(1017, 840));

    // Aşağıda, bir şekli Graphics nesnesine işlemek için "ShapeRenderer" sınıfını kullanmanın iki yolu bulunmaktadır.
    // 1 - Bir grafikle bir şekil oluştur ve onu belirli bir ölçeğe göre işle.
    Chart chart = builder.InsertChart(ChartType.Pie, 500, 400).Chart;
    chart.Series.Clear();
    chart.Series.Add("Desktop Browser Market Share (Oct. 2020)",
        new[] { "Google Chrome", "Apple Safari", "Mozilla Firefox", "Microsoft Edge", "Other" },
        new[] { 70.33, 8.87, 7.69, 5.83, 7.28 });

    Shape chartShape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

    shapeForm.AddShapeToRenderToScale(chartShape, 0, 0, 1.5f);

    // 2 - Bir şekil grubu oluştur ve onu belirli bir boyuta getir.
    GroupShape group = new GroupShape(doc);
    group.Bounds = new RectangleF(0, 0, 100, 100);
    group.CoordSize = new Size(500, 500);

    Shape subShape = new Shape(doc, ShapeType.Rectangle);
    subShape.Width = 500;
    subShape.Height = 500;
    subShape.Left = 0;
    subShape.Top = 0;
    subShape.FillColor = Color.RoyalBlue;
    group.AppendChild(subShape);

    subShape = new Shape(doc, ShapeType.Image);
    subShape.Width = 450;
    subShape.Height = 450;
    subShape.Left = 25;
    subShape.Top = 25;
    subShape.ImageData.SetImage(ImageDir + "Logo.jpg");
    group.AppendChild(subShape);

    builder.InsertNode(group);

    GroupShape groupShape = (GroupShape)doc.GetChild(NodeType.GroupShape, 0, true);
    shapeForm.AddShapeToRenderToSize(groupShape, 880, 680, 100, 100);

    shapeForm.ShowDialog();
}

/// <summary>
/// Şekillerin listesini oluşturur ve görüntüler.
/// </summary>
private class ShapeForm : Form
{
    public ShapeForm(Size size)
    {
        Size = size;
        mShapesToRender = new List<KeyValuePair<ShapeBase, float[]>>();
    }

    public void AddShapeToRenderToScale(ShapeBase shape, float x, float y, float scale)
    {
        mShapesToRender.Add(new KeyValuePair<ShapeBase, float[]>(shape, new[] {x, y, scale}));
    }

    public void AddShapeToRenderToSize(ShapeBase shape, float x, float y, float width, float height)
    {
        mShapesToRender.Add(new KeyValuePair<ShapeBase, float[]>(shape, new[] {x, y, width, height}));
    }

    protected override void OnPaint(PaintEventArgs e)
    {
        foreach (KeyValuePair<ShapeBase, float[]> renderingArgs in mShapesToRender)
            if (renderingArgs.Value.Length == 3)
                RenderShapeToScale(renderingArgs.Key, renderingArgs.Value[0], renderingArgs.Value[1],
                    renderingArgs.Value[2]);
            else if (renderingArgs.Value.Length == 4)
                RenderShapeToSize(renderingArgs.Key, renderingArgs.Value[0], renderingArgs.Value[1],
                    renderingArgs.Value[2], renderingArgs.Value[3]);
    }

    private void RenderShapeToScale(ShapeBase shape, float x, float y, float scale)
    {
        ShapeRenderer renderer = new ShapeRenderer(shape);
        using (Graphics formGraphics = CreateGraphics())
        {
            renderer.RenderToScale(formGraphics, x, y, scale);
        }
    }

    private void RenderShapeToSize(ShapeBase shape, float x, float y, float width, float height)
    {
        ShapeRenderer renderer = new ShapeRenderer(shape);
        using (Graphics formGraphics = CreateGraphics())
        {
            renderer.RenderToSize(formGraphics, x, y, width, height);
        }
    }

    private readonly List<KeyValuePair<ShapeBase, float[]>> mShapesToRender;
}
```

### Ayrıca bakınız

* class [NodeRendererBase](../)
* ad alanı [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* toplantı [Aspose.Words](../../../)
