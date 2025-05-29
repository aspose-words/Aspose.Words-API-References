---
title: RevisionColor Enum
linktitle: RevisionColor
articleTitle: RevisionColor
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words.Layout.RevisionColor para personalizar los colores de revisión del documento, mejorando la claridad y la colaboración en sus documentos.
type: docs
weight: 3830
url: /es/net/aspose.words.layout/revisioncolor/
---
## RevisionColor enumeration

Permite especificar el color de las revisiones del documento.

```csharp
public enum RevisionColor
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Auto | `0` | Predeterminado. |
| Black | `1` | Representa 000000 colores. |
| Blue | `2` | Representa el color 2e97d3. |
| BrightGreen | `3` | Representa el color 84a35b. |
| ClassicBlue | `4` | Representa el color 0000ff. |
| ClassicRed | `5` | Representa el color ff0000. |
| DarkBlue | `6` | Representa el color 376e96. |
| DarkRed | `7` | Representa 881824 colores. |
| DarkYellow | `8` | Representa el color e09a2b. |
| Gray25 | `9` | Representa un color 0a3a9. |
| Gray50 | `10` | Representa el color 50565e. |
| Green | `11` | Representa el color 2c6234. |
| Pink | `12` | Representa el color ce338f. |
| Red | `13` | Representa el color b5082e. |
| Teal | `14` | Representa el color 1b9cab. |
| Turquoise | `15` | Representa 3 colores EAFC2. |
| Violet | `16` | Representa 633277 colores. |
| White | `17` | Representa el color ffffff. |
| Yellow | `18` | Representa el color fad272. |
| LightPink | `19` | Representa el color fce6f4. |
| LightBlue | `20` | Representa el color e1f2fa. |
| LightYellow | `21` | Representa el color fef4de. |
| LightPurple | `22` | Representa el color eadfef. |
| LightOrange | `23` | Representa el color fce3d0. |
| LightGreen | `24` | Representa el color e9f8ce. |
| Gray | `25` | Representa el color real. |
| NoHighlight | `26` | No se utiliza ningún color para resaltar los cambios de revisión. |
| ByAuthor | `27` | Las revisiones de cada autor reciben su propio color para resaltar de un conjunto predefinido de colores de alto contraste. |

## Ejemplos

Muestra cómo alterar la apariencia de las revisiones en un documento de salida renderizado.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserte una revisión, luego cambie el color de todas las revisiones a verde.
builder.Writeln("This is not a revision.");
doc.StartTrackRevisions("John Doe", DateTime.Now);
builder.Writeln("This is a revision.");
doc.StopTrackRevisions();
builder.Writeln("This is not a revision.");

//Elimina la barra que aparece a la izquierda de cada línea revisada.
doc.LayoutOptions.RevisionOptions.InsertedTextColor = RevisionColor.BrightGreen;
doc.LayoutOptions.RevisionOptions.ShowRevisionBars = false;
doc.LayoutOptions.RevisionOptions.RevisionBarsPosition = HorizontalAlignment.Right;

doc.Save(ArtifactsDir + "Revision.LayoutOptionsRevisions.pdf");
```

### Ver también

* espacio de nombres [Aspose.Words.Layout](../../aspose.words.layout/)
* asamblea [Aspose.Words](../../)
