---
title: RevisionOptions.RevisedPropertiesEffect
linktitle: RevisedPropertiesEffect
articleTitle: RevisedPropertiesEffect
second_title: Aspose.Words para .NET
description: Descubra cómo el efecto RevisedPropertiesEffect de RevisionOptions mejora el formato de su contenido. Personalice fácilmente los cambios con la función FormatChange.
type: docs
weight: 140
url: /es/net/aspose.words.layout/revisionoptions/revisedpropertieseffect/
---
## RevisionOptions.RevisedPropertiesEffect property

Permite especificar el efecto para las áreas de contenido con cambios en las propiedades de formatoFormatChange El valor predeterminado esNone

```csharp
public RevisionTextEffect RevisedPropertiesEffect { get; set; }
```

### Excepciones

| excepción | condición |
| --- | --- |
| ArgumentOutOfRangeException | Hidden No está permitido. |

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

* enum [RevisionTextEffect](../../revisiontexteffect/)
* class [RevisionOptions](../)
* espacio de nombres [Aspose.Words.Layout](../../../aspose.words.layout/)
* asamblea [Aspose.Words](../../../)
