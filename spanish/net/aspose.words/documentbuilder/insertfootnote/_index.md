---
title: DocumentBuilder.InsertFootnote
second_title: Referencia de API de Aspose.Words para .NET
description: DocumentBuilder método. Inserta una nota al pie o una nota final en el documento.
type: docs
weight: 340
url: /es/net/aspose.words/documentbuilder/insertfootnote/
---
## InsertFootnote(FootnoteType, string) {#insertfootnote}

Inserta una nota al pie o una nota final en el documento.

```csharp
public Footnote InsertFootnote(FootnoteType footnoteType, string footnoteText)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| footnoteType | FootnoteType | Especifica si se inserta una nota al pie o una nota al final. |
| footnoteText | String | Especifica el texto de la nota al pie. |

### Valor_devuelto

Devuelve un objeto de nota al pie que se acaba de crear.

### Ejemplos

Muestra cómo hacer referencia al texto con una nota al pie y una nota al final.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserta algo de texto y márcalo con una nota al pie con la propiedad IsAuto establecida en "verdadero" de forma predeterminada,
// por lo que el marcador que se ve en el cuerpo del texto se numerará automáticamente en "1",
// y la nota al pie aparecerá al final de la página.
builder.Write("This text will be referenced by a footnote.");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote comment regarding referenced text.");

// Inserta más texto y márcalo con una nota al final con una marca de referencia personalizada,
// que se utilizará en lugar del número "2" y establecerá "IsAuto" en falso.
builder.Write("This text will be referenced by an endnote.");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote comment regarding referenced text.", "CustomMark");

// Las notas a pie de página siempre aparecen al final del texto al que se hace referencia,
// por lo que este salto de página no afectará a la nota al pie.
// Por otro lado, las notas finales siempre están al final del documento.
// para que este salto de página empuje la nota final a la página siguiente.
builder.InsertBreak(BreakType.PageBreak);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertFootnote.docx");
```

### Ver también

* class [Footnote](../../../aspose.words.notes/footnote/)
* enum [FootnoteType](../../../aspose.words.notes/footnotetype/)
* class [DocumentBuilder](../)
* espacio de nombres [Aspose.Words](../../documentbuilder/)
* asamblea [Aspose.Words](../../../)

---

## InsertFootnote(FootnoteType, string, string) {#insertfootnote_1}

Inserta una nota al pie o una nota final en el documento.

```csharp
public Footnote InsertFootnote(FootnoteType footnoteType, string footnoteText, string referenceMark)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| footnoteType | FootnoteType | Especifica si se inserta una nota al pie o una nota al final. |
| footnoteText | String | Especifica el texto de la nota al pie. |
| referenceMark | String | Especifica la marca de referencia personalizada de la nota al pie. |

### Valor_devuelto

Devuelve un objeto de nota al pie que se acaba de crear.

### Ejemplos

Muestra cómo hacer referencia al texto con una nota al pie y una nota al final.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserta algo de texto y márcalo con una nota al pie con la propiedad IsAuto establecida en "verdadero" de forma predeterminada,
// por lo que el marcador que se ve en el cuerpo del texto se numerará automáticamente en "1",
// y la nota al pie aparecerá al final de la página.
builder.Write("This text will be referenced by a footnote.");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote comment regarding referenced text.");

// Inserta más texto y márcalo con una nota al final con una marca de referencia personalizada,
// que se utilizará en lugar del número "2" y establecerá "IsAuto" en falso.
builder.Write("This text will be referenced by an endnote.");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote comment regarding referenced text.", "CustomMark");

// Las notas a pie de página siempre aparecen al final del texto al que se hace referencia,
// por lo que este salto de página no afectará a la nota al pie.
// Por otro lado, las notas finales siempre están al final del documento.
// para que este salto de página empuje la nota final a la página siguiente.
builder.InsertBreak(BreakType.PageBreak);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertFootnote.docx");
```

### Ver también

* class [Footnote](../../../aspose.words.notes/footnote/)
* enum [FootnoteType](../../../aspose.words.notes/footnotetype/)
* class [DocumentBuilder](../)
* espacio de nombres [Aspose.Words](../../documentbuilder/)
* asamblea [Aspose.Words](../../../)


