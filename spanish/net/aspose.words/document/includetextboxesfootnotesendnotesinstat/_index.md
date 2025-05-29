---
title: Document.IncludeTextboxesFootnotesEndnotesInStat
linktitle: IncludeTextboxesFootnotesEndnotesInStat
articleTitle: IncludeTextboxesFootnotesEndnotesInStat
second_title: Aspose.Words para .NET
description: Optimiza el número de palabras de tu documento con la propiedad IncludeTextboxesFootnotesEndnotesInStat. ¡Controla cuadros de texto, notas al pie y notas finales fácilmente!
type: docs
weight: 230
url: /es/net/aspose.words/document/includetextboxesfootnotesendnotesinstat/
---
## Document.IncludeTextboxesFootnotesEndnotesInStat property

Especifica si se deben incluir cuadros de texto, notas al pie y notas finales en las estadísticas de recuento de palabras.

```csharp
public bool IncludeTextboxesFootnotesEndnotesInStat { get; set; }
```

## Ejemplos

Muestra cómo incluir o excluir cuadros de texto, notas al pie y notas finales de las estadísticas de recuento de palabras.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Lorem ipsum");
builder.InsertFootnote(FootnoteType.Footnote, "sit amet");

//La opción predeterminada se establece en 'falso'.
doc.UpdateWordCount();
// Las palabras cuentan sin cuadros de texto, notas al pie y notas finales.
Assert.AreEqual(2, doc.BuiltInDocumentProperties.Words);

doc.IncludeTextboxesFootnotesEndnotesInStat = true;
doc.UpdateWordCount();
// Las palabras cuentan con cuadros de texto, notas al pie y notas finales.
Assert.AreEqual(4, doc.BuiltInDocumentProperties.Words);
```

### Ver también

* class [Document](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
