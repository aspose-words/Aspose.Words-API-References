---
title: Paragraph.GetEffectiveTabStops
linktitle: GetEffectiveTabStops
articleTitle: GetEffectiveTabStops
second_title: Aspose.Words para .NET
description: Descubra el método GetEffectiveTabStops para recuperar todas las tabulaciones de un párrafo, incluidas las de estilos y listas para un formato mejorado.
type: docs
weight: 270
url: /es/net/aspose.words/paragraph/geteffectivetabstops/
---
## Paragraph.GetEffectiveTabStops method

Devuelve una matriz de todas las tabulaciones aplicadas a este párrafo, incluidas las aplicadas indirectamente por estilos o listas.

```csharp
public TabStop[] GetEffectiveTabStops()
```

## Ejemplos

Muestra cómo establecer tabulaciones personalizadas para un párrafo.

```csharp
Document doc = new Document();
Paragraph para = doc.FirstSection.Body.FirstParagraph;

// Si estamos en un párrafo sin tabulaciones en esta colección,
//el cursor saltará 36 puntos cada vez que presionemos la tecla Tab en Microsoft Word.
Assert.AreEqual(0, doc.FirstSection.Body.FirstParagraph.GetEffectiveTabStops().Length);

//Podemos agregar tabulaciones personalizadas en Microsoft Word si habilitamos la regla a través de la pestaña "Ver".
// Cada unidad de esta regla son dos tabulaciones predeterminadas, que son 72 puntos.
//Podemos agregar tabulaciones personalizadas programáticamente de esta manera.
TabStopCollection tabStops = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.TabStops;
tabStops.Add(72, TabAlignment.Left, TabLeader.Dots);
tabStops.Add(216, TabAlignment.Center, TabLeader.Dashes);
tabStops.Add(360, TabAlignment.Right, TabLeader.Line);

//Podemos ver estas tabulaciones en Microsoft Word habilitando la regla a través de "Ver" -> "Mostrar" -> "Regla".
Assert.AreEqual(3, para.GetEffectiveTabStops().Length);

// Cualquier carácter de tabulación que agreguemos utilizará las tabulaciones de la regla y puede,
// dependiendo del valor del líder de la pestaña, deje una línea entre los destinos de salida y llegada de la pestaña.
para.AppendChild(new Run(doc, "\tTab 1\tTab 2\tTab 3"));

doc.Save(ArtifactsDir + "Paragraph.TabStops.docx");
```

### Ver también

* class [TabStop](../../tabstop/)
* class [Paragraph](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
