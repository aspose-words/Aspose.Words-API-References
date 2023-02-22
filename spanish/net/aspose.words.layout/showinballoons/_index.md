---
title: Enum ShowInBalloons
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Layout.ShowInBalloons enumeración. Especifica qué revisiones se representan en globos.
type: docs
weight: 3210
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
| None | `0` | Renderiza insertar, eliminar y dar formato a las revisiones en línea. |
| Format | `1` | Renderiza insertar y eliminar revisiones en línea, formatear revisiones en globos. |
| FormatAndDelete | `2` | Renderiza insertar revisiones en línea, eliminar y formatear revisiones en globos. |

### Observaciones

Tenga en cuenta que las revisiones no se representan en globos paraShowInAnnotations .

### Ejemplos

Muestra cómo modificar la apariencia de las revisiones.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

// Obtener el objeto RevisionOptions que controla la apariencia de las revisiones.
RevisionOptions revisionOptions = doc.LayoutOptions.RevisionOptions;

// Representar las revisiones de inserción en verde y cursiva.
revisionOptions.InsertedTextColor = RevisionColor.Green;
revisionOptions.InsertedTextEffect = RevisionTextEffect.Italic;

// Presentar las revisiones de eliminación en rojo y en negrita.
revisionOptions.DeletedTextColor = RevisionColor.Red;
revisionOptions.DeletedTextEffect = RevisionTextEffect.Bold;

// El mismo texto aparecerá dos veces en una revisión de movimiento:
// una vez en el punto de partida y una vez en el destino de llegada.
// Representar el texto en amarillo en la revisión desde la que se movió con un doble tachado
// y doble subrayado azul en la revisión a la que se movió.
revisionOptions.MovedFromTextColor = RevisionColor.Yellow;
revisionOptions.MovedFromTextEffect = RevisionTextEffect.DoubleStrikeThrough;
revisionOptions.MovedToTextColor = RevisionColor.Blue;
revisionOptions.MovedFromTextEffect = RevisionTextEffect.DoubleUnderline;

// Renderizar las revisiones del formato en rojo oscuro y en negrita.
revisionOptions.RevisedPropertiesColor = RevisionColor.DarkRed;
revisionOptions.RevisedPropertiesEffect = RevisionTextEffect.Bold;

// Coloque una barra gruesa de color azul oscuro en el lado izquierdo de la página junto a las líneas afectadas por las revisiones.
revisionOptions.RevisionBarsColor = RevisionColor.DarkBlue;
revisionOptions.RevisionBarsWidth = 15.0f;

// Mostrar marcas de revisión y texto original.
revisionOptions.ShowOriginalRevision = true;
revisionOptions.ShowRevisionMarks = true;

// Obtenga movimiento, eliminación, revisiones de formato y comentarios para mostrar en globos verdes
// en el lado derecho de la página.
revisionOptions.ShowInBalloons = ShowInBalloons.Format;
revisionOptions.CommentColor = RevisionColor.BrightGreen;

// Estas funciones solo se aplican a formatos como .pdf o .jpg.
doc.Save(ArtifactsDir + "Revision.RevisionOptions.pdf");
```

### Ver también

* espacio de nombres [Aspose.Words.Layout](../../aspose.words.layout/)
* asamblea [Aspose.Words](../../)


