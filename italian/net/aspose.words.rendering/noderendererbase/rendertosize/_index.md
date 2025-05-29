---
title: NodeRendererBase.RenderToSize
linktitle: RenderToSize
articleTitle: RenderToSize
second_title: Aspose.Words per .NET
description: Scopri il metodo RenderToSize di NodeRendererBase per trasformare in modo efficiente le forme in oggetti grafici nelle dimensioni desiderate, ottenendo così un output visivo migliore.
type: docs
weight: 80
url: /it/net/aspose.words.rendering/noderendererbase/rendertosize/
---
## NodeRendererBase.RenderToSize method

Rende la forma in unGraphics oggetto a una dimensione specificata.

```csharp
public float RenderToSize(Graphics graphics, float x, float y, float width, float height)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| graphics | Graphics | L'oggetto su cui effettuare il rendering. |
| x | Single | Coordinata X (in unità mondiali) dell'angolo in alto a sinistra della forma renderizzata. |
| y | Single | Coordinata Y (in unità mondiali) dell'angolo in alto a sinistra della forma renderizzata. |
| width | Single | Larghezza massima (in unità mondiali) che può essere occupata dalla forma renderizzata. |
| height | Single | L'altezza massima (in unità mondiali) che può essere occupata dalla forma renderizzata. |

### Valore di ritorno

La scala calcolata automaticamente per adattare la forma renderizzata alle dimensioni specificate.

## Esempi

Mostra come eseguire il rendering di una forma con un oggetto Graphics e visualizzarla utilizzando un Windows Form.

```csharp
public void RenderShapesOnForm()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    ShapeForm shapeForm = new ShapeForm(new Size(1017, 840));

    // Di seguito sono riportati due modi per utilizzare la classe "ShapeRenderer" per eseguire il rendering di una forma in un oggetto Graphics.
    // 1 - Crea una forma con un grafico e visualizzala in una scala specifica.
    Chart chart = builder.InsertChart(ChartType.Pie, 500, 400).Chart;
    chart.Series.Clear();
    chart.Series.Add("Desktop Browser Market Share (Oct. 2020)",
        new[] { "Google Chrome", "Apple Safari", "Mozilla Firefox", "Microsoft Edge", "Other" },
        new[] { 70.33, 8.87, 7.69, 5.83, 7.28 });

    Shape chartShape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

    shapeForm.AddShapeToRenderToScale(chartShape, 0, 0, 1.5f);

    // 2 - Crea un gruppo di forme e rendilo di una dimensione specifica.
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
/// Esegue il rendering e visualizza un elenco di forme.
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

### Guarda anche

* class [NodeRendererBase](../)
* spazio dei nomi [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* assemblea [Aspose.Words](../../../)
