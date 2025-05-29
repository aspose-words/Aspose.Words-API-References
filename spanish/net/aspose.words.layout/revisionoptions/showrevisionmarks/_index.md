---
title: RevisionOptions.ShowRevisionMarks
linktitle: ShowRevisionMarks
articleTitle: ShowRevisionMarks
second_title: Aspose.Words para .NET
description: Controle la visibilidad de las revisiones con la propiedad ShowRevisionMarks. Formatee fácilmente el texto de las revisiones para mayor claridad, lo que mejora la colaboración en el documento. El valor predeterminado es "true".
type: docs
weight: 210
url: /es/net/aspose.words.layout/revisionoptions/showrevisionmarks/
---
## RevisionOptions.ShowRevisionMarks property

Permite especificar si el texto de revisión debe marcarse con un marcado de formato especial. El valor predeterminado es`verdadero` .

```csharp
public bool ShowRevisionMarks { get; set; }
```

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

* class [RevisionOptions](../)
* espacio de nombres [Aspose.Words.Layout](../../../aspose.words.layout/)
* asamblea [Aspose.Words](../../../)
