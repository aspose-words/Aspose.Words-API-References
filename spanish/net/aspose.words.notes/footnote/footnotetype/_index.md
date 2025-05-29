---
title: Footnote.FootnoteType
linktitle: FootnoteType
articleTitle: FootnoteType
second_title: Aspose.Words para .NET
description: Descubra la propiedad FootnoteType, identifique fácilmente notas al pie o notas finales en sus documentos para una mayor claridad y organización.
type: docs
weight: 30
url: /es/net/aspose.words.notes/footnote/footnotetype/
---
## Footnote.FootnoteType property

Devuelve un valor que especifica si se trata de una nota al pie o una nota final.

```csharp
public FootnoteType FootnoteType { get; }
```

## Ejemplos

Muestra la diferencia entre notas al pie y notas finales.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

A continuación se presentan dos formas de adjuntar referencias numeradas al texto. Ambas referencias añadirán un...
// Pequeña marca de referencia superíndice en la ubicación donde los insertamos.
//La marca de referencia, por defecto, es el número de índice de la referencia entre todas las referencias del documento.
// Cada referencia también creará una entrada, que tendrá la misma marca de referencia que en el cuerpo del texto.
// y texto de referencia, que pasaremos al método "InsertFootnote" del generador de documentos.
// 1 - Una nota a pie de página, cuya entrada aparecerá en la misma página que el texto al que hace referencia:
builder.Write("Footnote referenced main body text.");
Footnote footnote = builder.InsertFootnote(FootnoteType.Footnote, 
    "Footnote text, will appear at the bottom of the page that contains the referenced text.");

// 2 - Una nota final, cuya entrada aparecerá al final del documento:
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
* espacio de nombres [Aspose.Words.Notes](../../../aspose.words.notes/)
* asamblea [Aspose.Words](../../../)
