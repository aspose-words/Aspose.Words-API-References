---
title: Paragraph.GetEffectiveTabStops
second_title: Referencia de API de Aspose.Words para .NET
description: Paragraph método. Devuelve una matriz de todas las tabulaciones aplicadas a este párrafo incluidas las aplicadas indirectamente por estilos o listas.
type: docs
weight: 250
url: /es/net/aspose.words/paragraph/geteffectivetabstops/
---
## Paragraph.GetEffectiveTabStops method

Devuelve una matriz de todas las tabulaciones aplicadas a este párrafo, incluidas las aplicadas indirectamente por estilos o listas.

```csharp
public TabStop[] GetEffectiveTabStops()
```

### Ejemplos

Muestra cómo establecer tabulaciones personalizadas para un párrafo.

```csharp
Document doc = new Document();
Paragraph para = doc.FirstSection.Body.FirstParagraph;

// Si estamos en un párrafo sin tabulaciones en esta colección,
// el cursor saltará 36 puntos cada vez que presionemos la tecla Tab en Microsoft Word.
Assert.AreEqual(0, doc.FirstSection.Body.FirstParagraph.GetEffectiveTabStops().Length);

// Podemos agregar tabulaciones personalizadas en Microsoft Word si habilitamos la regla a través de la pestaña "Ver".
// Cada unidad en esta regla son dos tabulaciones predeterminadas, que son 72 puntos.
// Podemos agregar tabulaciones personalizadas programáticamente como esta.
TabStopCollection tabStops = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.TabStops;
tabStops.Add(72, TabAlignment.Left, TabLeader.Dots);
tabStops.Add(216, TabAlignment.Center, TabLeader.Dashes);
tabStops.Add(360, TabAlignment.Right, TabLeader.Line);

// Podemos ver estas tabulaciones en Microsoft Word activando la regla a través de "Ver" -> "Mostrar" -> "Gobernante".
Assert.AreEqual(3, para.GetEffectiveTabStops().Length);

// Cualquier carácter de tabulación que agreguemos hará uso de las tabulaciones en la regla y puede,
// dependiendo del valor del líder de la pestaña, deje una línea entre los destinos de salida y llegada de la pestaña.
para.AppendChild(new Run(doc, "\tTab 1\tTab 2\tTab 3"));

doc.Save(ArtifactsDir + "Paragraph.TabStops.docx");
```

### Ver también

* class [TabStop](../../tabstop/)
* class [Paragraph](../)
* espacio de nombres [Aspose.Words](../../paragraph/)
* asamblea [Aspose.Words](../../../)


