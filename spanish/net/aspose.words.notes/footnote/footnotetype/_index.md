---
title: Footnote.FootnoteType
second_title: Referencia de API de Aspose.Words para .NET
description: Footnote propiedad. Devuelve un valor que especifica si se trata de una nota al pie o al final.
type: docs
weight: 20
url: /es/net/aspose.words.notes/footnote/footnotetype/
---
## Footnote.FootnoteType property

Devuelve un valor que especifica si se trata de una nota al pie o al final.

```csharp
public FootnoteType FootnoteType { get; }
```

### Ejemplos

Muestra la diferencia entre notas al pie y notas al final.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// A continuación se muestran dos formas de adjuntar referencias numeradas al texto. Ambas referencias agregarán un
// pequeña marca de referencia en superíndice en la ubicación en la que los insertamos.
// La marca de referencia, por defecto, es el número de índice de la referencia entre todas las referencias del documento.
// Cada referencia también creará una entrada, que tendrá la misma marca de referencia que en el cuerpo del texto
// y texto de referencia, que pasaremos al método "InsertFootnote" del generador de documentos.
// 1 - Una nota al pie, cuya entrada aparecerá en la misma página que el texto al que hace referencia:
builder.Write("Footnote referenced main body text.");
Footnote footnote = builder.InsertFootnote(FootnoteType.Footnote, 
    "Footnote text, will appear at the bottom of the page that contains the referenced text.");

// 2 - Una nota al final, cuya entrada aparecerá al final del documento:
builder.Write("Endnote referenced main body text.");
Footnote endnote = builder.InsertFootnote(FootnoteType.Endnote, 
    "Endnote text, will appear at the very end of the document.");

builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.InsertBreak(BreakType.SectionBreakNewPage);

Assert.AreEqual(FootnoteType.Footnote, footnote.FootnoteType);
Assert.AreEqual(FootnoteType.Endnote, endnote.FootnoteType);

doc.Save(ArtifactsDir + "InlineStory.FootnoteEndnote.docx");
```

### Ver también

* enum [FootnoteType](../../footnotetype/)
* class [Footnote](../)
* espacio de nombres [Aspose.Words.Notes](../../footnote/)
* asamblea [Aspose.Words](../../../)


