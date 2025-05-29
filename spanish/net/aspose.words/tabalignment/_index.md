---
title: TabAlignment Enum
linktitle: TabAlignment
articleTitle: TabAlignment
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words.TabAlignment para personalizar la alineación de tabulaciones. ¡Mejore el formato de sus documentos con precisión y flexibilidad hoy mismo!
type: docs
weight: 7030
url: /es/net/aspose.words/tabalignment/
---
## TabAlignment enumeration

Especifica la alineación/tipo de una tabulación.

```csharp
public enum TabAlignment
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Left | `0` | Alinea a la izquierda el texto después de la tabulación. |
| Center | `1` | Centra el texto alrededor de la tabulación. |
| Right | `2` | Alinea a la derecha el texto en la tabulación. |
| Decimal | `3` | Alinea el texto en el punto decimal. |
| Bar | `4` | Dibuja una barra vertical en la posición de tabulación. |
| List | `6` | La tabulación es un delimitador entre el número/viñeta y el texto en un elemento de lista. |
| Clear | `7` | Borra cualquier tabulación en esta posición. |

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

* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)
