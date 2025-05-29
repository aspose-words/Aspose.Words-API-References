---
title: FootnoteNumberingRule Enum
linktitle: FootnoteNumberingRule
articleTitle: FootnoteNumberingRule
second_title: Aspose.Words para .NET
description: Descubra la enumeración FootnoteNumberingRule de Aspose.Words para controlar la numeración automática de notas al pie y al final. ¡Optimice el formato de sus documentos fácilmente!
type: docs
weight: 4960
url: /es/net/aspose.words.notes/footnotenumberingrule/
---
## FootnoteNumberingRule enumeration

Determina cuándo se reinicia la numeración automática de notas al pie o notas finales.

```csharp
public enum FootnoteNumberingRule
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Continuous | `0` | Numeración continua en todo el documento. |
| RestartSection | `1` | La numeración se reinicia en cada sección. |
| RestartPage | `2` | La numeración se reinicia en cada página. Válido solo para notas al pie. |
| Default | `0` | Es igual aContinuous . |

## Ejemplos

Muestra cómo reiniciar la numeración de notas al pie y notas finales en determinados lugares del documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Las notas a pie de página y las notas finales son una forma de adjuntar una referencia o un comentario al margen del texto.
 // que no interfiera con el flujo del texto del cuerpo principal.
// Insertar una nota al pie o una nota final agrega un pequeño símbolo de referencia en superíndice
// en el cuerpo principal del texto donde insertamos la nota al pie/nota final.
// Cada nota al pie/nota final también crea una entrada, que consiste en un símbolo que coincide con la referencia.
// Símbolo en el cuerpo principal del texto. El texto de referencia que pasamos al método "InsertEndnote" del generador de documentos.
// Las entradas de notas al pie, de forma predeterminada, aparecen en la parte inferior de cada página que contiene
// sus símbolos de referencia y notas finales aparecen al final del documento.
builder.Write("Text 1. ");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote 1.");
builder.Write("Text 2. ");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote 2.");
builder.InsertBreak(BreakType.PageBreak);
builder.Write("Text 3. ");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote 3.");
builder.Write("Text 4. ");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote 4.");

builder.InsertBreak(BreakType.PageBreak);

builder.Write("Text 1. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 1.");
builder.Write("Text 2. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 2.");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Text 3. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 3.");
builder.Write("Text 4. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 4.");

// De forma predeterminada, el símbolo de referencia para cada nota al pie y nota final es su índice.
// entre todas las notas al pie y al final del documento. Cada documento mantiene recuentos separados.
// para notas al pie y notas finales y no reinicia estos recuentos en ningún momento.
Assert.AreEqual(doc.FootnoteOptions.RestartRule, FootnoteNumberingRule.Default);
Assert.AreEqual(FootnoteNumberingRule.Default, FootnoteNumberingRule.Continuous);

// Podemos usar la propiedad "RestartRule" para que el documento se reinicie
// La nota al pie o nota final cuenta en una nueva página o sección.
doc.FootnoteOptions.RestartRule = FootnoteNumberingRule.RestartPage;
doc.EndnoteOptions.RestartRule = FootnoteNumberingRule.RestartSection;

doc.Save(ArtifactsDir + "InlineStory.NumberingRule.docx");
```

### Ver también

* class [FootnoteOptions](../footnoteoptions/)
* class [EndnoteOptions](../endnoteoptions/)
* espacio de nombres [Aspose.Words.Notes](../../aspose.words.notes/)
* asamblea [Aspose.Words](../../)
