---
title: Fill.Solid
second_title: Referencia de API de Aspose.Words para .NET
description: Fill método. Establece el relleno en un color uniforme.
type: docs
weight: 260
url: /es/net/aspose.words.drawing/fill/solid/
---
## Solid() {#solid}

Establece el relleno en un color uniforme.

```csharp
public void Solid()
```

### Observaciones

Utilice este método para convertir cualquiera de los rellenos a relleno sólido.

### Ver también

* class [Fill](../)
* espacio de nombres [Aspose.Words.Drawing](../../fill/)
* asamblea [Aspose.Words](../../../)

---

## Solid(Color) {#solid_1}

Establece el relleno en un color uniforme especificado.

```csharp
public void Solid(Color color)
```

### Observaciones

Utilice este método para convertir cualquiera de los rellenos a relleno sólido.

### Ejemplos

Muestra cómo convertir cualquiera de los rellenos a relleno sólido.

```csharp
Document doc = new Document(MyDir + "Two color gradient.docx");

// Obtiene el objeto de relleno para la fuente de la primera ejecución.
Fill fill = doc.FirstSection.Body.Paragraphs[0].Runs[0].Font.Fill;

// Verifique las propiedades de relleno de la fuente.
Console.WriteLine("The type of the fill is: {0}", fill.FillType);
Console.WriteLine("The foreground color of the fill is: {0}", fill.ForeColor);
Console.WriteLine("The fill is transparent at {0}%", fill.Transparency * 100);

// Cambia el tipo de relleno a Sólido con color verde uniforme.
fill.Solid(Color.Green);
Console.WriteLine("\nThe fill is changed:");
Console.WriteLine("The type of the fill is: {0}", fill.FillType);
Console.WriteLine("The foreground color of the fill is: {0}", fill.ForeColor);
Console.WriteLine("The fill transparency is {0}%", fill.Transparency * 100);

doc.Save(ArtifactsDir + "Drawing.FillSolid.docx");
```

### Ver también

* class [Fill](../)
* espacio de nombres [Aspose.Words.Drawing](../../fill/)
* asamblea [Aspose.Words](../../../)


