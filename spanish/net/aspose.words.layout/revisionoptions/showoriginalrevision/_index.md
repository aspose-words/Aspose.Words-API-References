---
title: RevisionOptions.ShowOriginalRevision
second_title: Referencia de API de Aspose.Words para .NET
description: RevisionOptions propiedad. Permite especificar si se debe mostrar el texto original en lugar del revisado. El valor predeterminado esFALSO .
type: docs
weight: 170
url: /es/net/aspose.words.layout/revisionoptions/showoriginalrevision/
---
## RevisionOptions.ShowOriginalRevision property

Permite especificar si se debe mostrar el texto original en lugar del revisado. El valor predeterminado es`FALSO` .

```csharp
public bool ShowOriginalRevision { get; set; }
```

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

* class [RevisionOptions](../)
* espacio de nombres [Aspose.Words.Layout](../../revisionoptions/)
* asamblea [Aspose.Words](../../../)


