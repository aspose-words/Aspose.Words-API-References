---
title: Document.IncludeTextboxesFootnotesEndnotesInStat
second_title: Referencia de API de Aspose.Words para .NET
description: Document propiedad. Especifica si se incluyen cuadros de texto notas al pie y notas finales en las estadísticas de recuento de palabras.
type: docs
weight: 220
url: /es/net/aspose.words/document/includetextboxesfootnotesendnotesinstat/
---
## Document.IncludeTextboxesFootnotesEndnotesInStat property

Especifica si se incluyen cuadros de texto, notas al pie y notas finales en las estadísticas de recuento de palabras.

```csharp
public bool IncludeTextboxesFootnotesEndnotesInStat { get; set; }
```

### Ejemplos

Muestra cómo incluir o excluir cuadros de texto, notas al pie y notas al final de las estadísticas de recuento de palabras.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Lorem ipsum");
builder.InsertFootnote(FootnoteType.Footnote, "sit amet");

// Por defecto, la opción está configurada en 'falso'.
doc.UpdateWordCount();
// Las palabras cuentan sin cuadros de texto, notas al pie ni notas finales.
Assert.AreEqual(2, doc.BuiltInDocumentProperties.Words);            

doc.IncludeTextboxesFootnotesEndnotesInStat = true;
doc.UpdateWordCount();
// Las palabras cuentan con cuadros de texto, notas al pie y notas al final.
Assert.AreEqual(4, doc.BuiltInDocumentProperties.Words);
```

### Ver también

* class [Document](../)
* espacio de nombres [Aspose.Words](../../document/)
* asamblea [Aspose.Words](../../../)


