---
title: Enum ShowInBalloons
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Layout.ShowInBalloons enumeración. Especifica qué revisiones se representan en globos.
type: docs
weight: 3410
url: /es/net/aspose.words.layout/showinballoons/
---
## ShowInBalloons enumeration

Especifica qué revisiones se representan en globos.

```csharp
public enum ShowInBalloons
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| None | `0` | Representa las revisiones de inserción, eliminación y formato en línea. |
| Format | `1` | Representa la inserción y eliminación de revisiones en línea, formatea las revisiones en globos. |
| FormatAndDelete | `2` | Procesa insertar revisiones en línea, eliminar y formatear revisiones en globos. |

### Observaciones

Tenga en cuenta que las revisiones no se representan en globos paraShowInAnnotations .

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


