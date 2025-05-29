---
title: BorderCollection.GetEnumerator
linktitle: GetEnumerator
articleTitle: GetEnumerator
second_title: Aspose.Words para .NET
description: Descubra el método GetEnumerator de BorderCollection para iterar fácilmente a través de todos los bordes, mejorando la eficiencia de su codificación y la gestión de colecciones.
type: docs
weight: 160
url: /es/net/aspose.words/bordercollection/getenumerator/
---
## BorderCollection.GetEnumerator method

Devuelve un objeto enumerador que se puede utilizar para iterar sobre todos los bordes de la colección.

```csharp
public IEnumerator<Border> GetEnumerator()
```

## Ejemplos

Muestra cómo iterar y editar todos los bordes en un objeto de formato de párrafo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Configure los ajustes de formato de párrafo del constructor para crear un borde de onda verde en todos los lados.
BorderCollection borders = builder.ParagraphFormat.Borders;

using (IEnumerator<Border> enumerator = borders.GetEnumerator())
{
    while (enumerator.MoveNext())
    {
        Border border = enumerator.Current;
        border.Color = Color.Green;
        border.LineStyle = LineStyle.Wave;
        border.LineWidth = 3;
    }
}

Insertar un párrafo. La configuración del borde determinará su apariencia.
builder.Writeln("Hello world!");

doc.Save(ArtifactsDir + "BorderCollection.GetBordersEnumerator.docx");
```

### Ver también

* class [Border](../../border/)
* class [BorderCollection](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
