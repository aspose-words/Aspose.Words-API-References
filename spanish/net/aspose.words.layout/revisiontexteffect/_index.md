---
title: Enum RevisionTextEffect
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Layout.RevisionTextEffect enumeración. Permite especificar el efecto de decoración para revisiones del texto del documento.
type: docs
weight: 3400
url: /es/net/aspose.words.layout/revisiontexteffect/
---
## RevisionTextEffect enumeration

Permite especificar el efecto de decoración para revisiones del texto del documento.

```csharp
public enum RevisionTextEffect
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| None | `0` | El contenido revisado no tiene efectos especiales aplicados. Esto corresponde aNoHighlight . |
| Color | `1` | El contenido revisado se resalta solo con color. |
| Bold | `2` | El contenido revisado está en negrita y coloreado. |
| Italic | `3` | El contenido revisado está en cursiva y coloreado. |
| Underline | `4` | El contenido revisado está subrayado y coloreado. |
| DoubleUnderline | `5` | El contenido revisado está doblemente subrayado y coloreado. |
| StrikeThrough | `6` | El contenido revisado está tachado y coloreado. |
| DoubleStrikeThrough | `7` | El contenido revisado está doble trazo y coloreado. |
| Hidden | `8` | El contenido revisado está oculto. |

### Ejemplos

Muestra cómo modificar la apariencia de las revisiones.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

// Obtiene el objeto RevisionOptions que controla la apariencia de las revisiones.
RevisionOptions revisionOptions = doc.LayoutOptions.RevisionOptions;

// Representar revisiones de inserción en verde y cursiva.
revisionOptions.InsertedTextColor = RevisionColor.Green;
revisionOptions.InsertedTextEffect = RevisionTextEffect.Italic;

// Representar las revisiones eliminadas en rojo y negrita.
revisionOptions.DeletedTextColor = RevisionColor.Red;
revisionOptions.DeletedTextEffect = RevisionTextEffect.Bold;

// El mismo texto aparecerá dos veces en una revisión de movimiento:
// una vez en el punto de partida y otra en el destino de llegada.
// Representa el texto en la revisión de origen en amarillo con un doble tachado
// y azul con doble subrayado en la revisión a la que se trasladó.
revisionOptions.MovedFromTextColor = RevisionColor.Yellow;
revisionOptions.MovedFromTextEffect = RevisionTextEffect.DoubleStrikeThrough;
revisionOptions.MovedToTextColor = RevisionColor.ClassicBlue;
revisionOptions.MovedFromTextEffect = RevisionTextEffect.DoubleUnderline;

// Representar las revisiones de formato en rojo oscuro y negrita.
revisionOptions.RevisedPropertiesColor = RevisionColor.DarkRed;
revisionOptions.RevisedPropertiesEffect = RevisionTextEffect.Bold;

// Coloque una barra gruesa de color azul oscuro en el lado izquierdo de la página junto a las líneas afectadas por las revisiones.
revisionOptions.RevisionBarsColor = RevisionColor.DarkBlue;
revisionOptions.RevisionBarsWidth = 15.0f;

// Mostrar marcas de revisión y texto original.
revisionOptions.ShowOriginalRevision = true;
revisionOptions.ShowRevisionMarks = true;

// Obtener movimientos, eliminaciones, revisiones de formato y comentarios para que aparezcan en globos verdes
// en el lado derecho de la página.
revisionOptions.ShowInBalloons = ShowInBalloons.Format;
revisionOptions.CommentColor = RevisionColor.BrightGreen;

// Estas características sólo son aplicables a formatos como .pdf o .jpg.
doc.Save(ArtifactsDir + "Revision.RevisionOptions.pdf");
```

### Ver también

* espacio de nombres [Aspose.Words.Layout](../../aspose.words.layout/)
* asamblea [Aspose.Words](../../)


