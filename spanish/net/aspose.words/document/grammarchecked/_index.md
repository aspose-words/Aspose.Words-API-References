---
title: Document.GrammarChecked
linktitle: GrammarChecked
articleTitle: GrammarChecked
second_title: Aspose.Words para .NET
description: Garantice la calidad de su documento con la propiedad GrammarChecked. Descubra si su texto está gramaticalmente correcto para obtener resultados impecables y profesionales.
type: docs
weight: 190
url: /es/net/aspose.words/document/grammarchecked/
---
## Document.GrammarChecked property

Devuelve`verdadero` Si el documento ha sido revisado gramaticalmente.

```csharp
public bool GrammarChecked { get; set; }
```

## Observaciones

Para volver a verificar la gramática en el documento, configure esta propiedad en`FALSO` .

## Ejemplos

Muestra cómo configurar la verificación ortográfica o gramatical.

```csharp
Document doc = new Document();

//La cadena con errores ortográficos.
doc.FirstSection.Body.FirstParagraph.Runs.Add(new Run(doc, "The speeling in this documentz is all broked."));

// La verificación ortográfica y gramatical comienza si establecemos las propiedades como falsas.
//Podemos ver todos los errores en Microsoft Word a través de Revisar -> Ortografía y gramática.
// Tenga en cuenta que Microsoft Word no inicia automáticamente la revisión gramatical y ortográfica para los formatos de documentos DOC y RTF.
doc.SpellingChecked = checkSpellingGrammar;
doc.GrammarChecked = checkSpellingGrammar;

doc.Save(ArtifactsDir + "Document.SpellingOrGrammar.docx");
```

### Ver también

* class [Document](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
