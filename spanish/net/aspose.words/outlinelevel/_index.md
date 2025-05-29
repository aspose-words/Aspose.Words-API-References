---
title: OutlineLevel Enum
linktitle: OutlineLevel
articleTitle: OutlineLevel
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words.OutlineLevel para administrar fácilmente los niveles de esquema de párrafo en sus documentos para una mejor organización y claridad.
type: docs
weight: 5060
url: /es/net/aspose.words/outlinelevel/
---
## OutlineLevel enumeration

Especifica el nivel de esquema de un párrafo en el documento.

```csharp
public enum OutlineLevel
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Level1 | `0` | El párrafo está en el nivel de esquema 1 (nivel superior). |
| Level2 | `1` | El párrafo está en el nivel de esquema 2. |
| Level3 | `2` | El párrafo está en el nivel de esquema 3. |
| Level4 | `3` | El párrafo está en el nivel de esquema 4. |
| Level5 | `4` | El párrafo está en el nivel de esquema 5. |
| Level6 | `5` | El párrafo está en el nivel de esquema 6. |
| Level7 | `6` | El párrafo está en el nivel de esquema 7. |
| Level8 | `7` | El párrafo está en el nivel de esquema 8. |
| Level9 | `8` | El párrafo está en el nivel de esquema 9. |
| BodyText | `9` | El párrafo está al nivel del texto principal. |

## Ejemplos

Muestra cómo configurar los niveles de esquema de párrafo para crear texto contraíble.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Cada párrafo tiene un OutlineLevel, que puede ser cualquier número del 1 al 9, o el valor predeterminado "BodyText".
// Al establecer la propiedad en uno de los valores numerados se mostrará una flecha hacia la izquierda
// del inicio del párrafo.
builder.ParagraphFormat.OutlineLevel = OutlineLevel.Level1;
builder.Writeln("Paragraph outline level 1.");

// El nivel 1 es el más alto. Si hay un párrafo de nivel inferior debajo de otro de nivel superior,
// Al contraer el párrafo de nivel superior se contraerá el párrafo de nivel inferior.
builder.ParagraphFormat.OutlineLevel = OutlineLevel.Level2;
builder.Writeln("Paragraph outline level 2.");

// Dos párrafos del mismo nivel no se colapsarán entre sí,
// y las flechas no colapsan los párrafos a los que apuntan.
builder.ParagraphFormat.OutlineLevel = OutlineLevel.Level3;
builder.Writeln("Paragraph outline level 3.");
builder.Writeln("Paragraph outline level 3.");

// El valor predeterminado de "BodyText" es el más bajo que puede contraer un párrafo de cualquier nivel.
builder.ParagraphFormat.OutlineLevel = OutlineLevel.BodyText;
builder.Writeln("Paragraph at main text level.");

doc.Save(ArtifactsDir + "ParagraphFormat.ParagraphOutlineLevel.docx");
```

### Ver también

* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)
