---
title: RevisionOptions.CommentColor
linktitle: CommentColor
articleTitle: CommentColor
second_title: Aspose.Words para .NET
description: Personaliza tus comentarios con la propiedad CommentColor de RevisionOptions. Define fácilmente tu color preferido (el predeterminado es rojo) para una mejor visibilidad.
type: docs
weight: 10
url: /es/net/aspose.words.layout/revisionoptions/commentcolor/
---
## RevisionOptions.CommentColor property

Permite especificar el color que se utilizará para los comentarios. El valor predeterminado esRed .

```csharp
public RevisionColor CommentColor { get; set; }
```

## Observaciones

Si se establece esta propiedad enByAuthor oNoHighlight valores, como resultado, esta propiedad se establecerá en el color predeterminado.

## Ejemplos

Muestra cómo modificar la apariencia de las revisiones.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

// Obtenga el objeto RevisionOptions que controla la apariencia de las revisiones.
RevisionOptions revisionOptions = doc.LayoutOptions.RevisionOptions;

// Representar las revisiones de inserción en verde y cursiva.
revisionOptions.InsertedTextColor = RevisionColor.Green;
revisionOptions.InsertedTextEffect = RevisionTextEffect.Italic;

// Representar las revisiones de eliminación en rojo y negrita.
revisionOptions.DeletedTextColor = RevisionColor.Red;
revisionOptions.DeletedTextEffect = RevisionTextEffect.Bold;

//El mismo texto aparecerá dos veces en una revisión de movimiento:
// una vez en el punto de partida y otra vez en el destino de llegada.
// Representar el texto en la revisión movida en amarillo con un doble tachado
// y doble subrayado azul en la revisión trasladada.
revisionOptions.MovedFromTextColor = RevisionColor.Yellow;
revisionOptions.MovedFromTextEffect = RevisionTextEffect.DoubleStrikeThrough;
revisionOptions.MovedToTextColor = RevisionColor.ClassicBlue;
revisionOptions.MovedToTextEffect = RevisionTextEffect.DoubleUnderline;

// Representar las revisiones de formato en rojo oscuro y negrita.
revisionOptions.RevisedPropertiesColor = RevisionColor.DarkRed;
revisionOptions.RevisedPropertiesEffect = RevisionTextEffect.Bold;

// Coloque una barra gruesa de color azul oscuro en el lado izquierdo de la página junto a las líneas afectadas por las revisiones.
revisionOptions.RevisionBarsColor = RevisionColor.DarkBlue;
revisionOptions.RevisionBarsWidth = 15.0f;

// Mostrar marcas de revisión y texto original.
revisionOptions.ShowOriginalRevision = true;
revisionOptions.ShowRevisionMarks = true;

// Haga que el movimiento, la eliminación, las revisiones de formato y los comentarios aparezcan en globos verdes
// en el lado derecho de la página.
revisionOptions.ShowInBalloons = ShowInBalloons.Format;
revisionOptions.CommentColor = RevisionColor.BrightGreen;

// Estas características sólo son aplicables a formatos como .pdf o .jpg.
doc.Save(ArtifactsDir + "Revision.RevisionOptions.pdf");
```

### Ver también

* enum [RevisionColor](../../revisioncolor/)
* class [RevisionOptions](../)
* espacio de nombres [Aspose.Words.Layout](../../../aspose.words.layout/)
* asamblea [Aspose.Words](../../../)
