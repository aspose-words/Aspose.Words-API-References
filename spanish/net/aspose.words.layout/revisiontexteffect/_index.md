---
title: RevisionTextEffect Enum
linktitle: RevisionTextEffect
articleTitle: RevisionTextEffect
second_title: Aspose.Words para .NET
description: Descubre la enumeración Aspose.Words.Layout.RevisionTextEffect para mejorar las revisiones de documentos con efectos únicos de decoración de texto. ¡Mejora tu experiencia de edición!
type: docs
weight: 3850
url: /es/net/aspose.words.layout/revisiontexteffect/
---
## RevisionTextEffect enumeration

Permite especificar el efecto de decoración para las revisiones del texto del documento.

```csharp
public enum RevisionTextEffect
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| None | `0` | El contenido revisado no tiene efectos especiales aplicados. Esto corresponde aNoHighlight . |
| Color | `1` | El contenido revisado se resalta solo con color. |
| Bold | `2` | El contenido revisado se pone en negrita y color. |
| Italic | `3` | El contenido revisado se pone en cursiva y coloreado. |
| Underline | `4` | El contenido revisado está subrayado y coloreado. |
| DoubleUnderline | `5` | El contenido revisado está subrayado doblemente y coloreado. |
| StrikeThrough | `6` | El contenido revisado está trazado y coloreado. |
| DoubleStrikeThrough | `7` | El contenido revisado está tachado dos veces y coloreado. |
| Hidden | `8` | El contenido revisado está oculto. |

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

* espacio de nombres [Aspose.Words.Layout](../../aspose.words.layout/)
* asamblea [Aspose.Words](../../)
