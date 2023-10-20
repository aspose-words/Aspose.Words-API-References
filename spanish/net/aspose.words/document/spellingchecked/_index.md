---
title: Document.SpellingChecked
linktitle: SpellingChecked
articleTitle: SpellingChecked
second_title: Aspose.Words para .NET
description: Document SpellingChecked propiedad. Devolucionesverdadero si se ha revisado la ortografía del documento en C#.
type: docs
weight: 410
url: /es/net/aspose.words/document/spellingchecked/
---
## Document.SpellingChecked property

Devoluciones`verdadero` si se ha revisado la ortografía del documento.

```csharp
public bool SpellingChecked { get; set; }
```

## Observaciones

Para volver a revisar la ortografía del documento, establezca esta propiedad en`FALSO` .

## Ejemplos

Muestra cómo configurar la verificación ortográfica o gramatical.

```csharp
Document doc = new Document();

// La cadena con errores ortográficos.
doc.FirstSection.Body.FirstParagraph.Runs.Add(new Run(doc, "The speeling in this documentz is all broked."));

 // La revisión ortográfica/gramatical comienza si configuramos las propiedades en falso.
// Podemos ver todos los errores en Microsoft Word mediante Revisar -> Ortografía y Gramática.
// Tenga en cuenta que Microsoft Word no inicia la revisión gramatical/ortográfica automáticamente para los formatos de documentos DOC y RTF.
doc.SpellingChecked = checkSpellingGrammar;
doc.GrammarChecked = checkSpellingGrammar;

doc.Save(ArtifactsDir + "Document.SpellingOrGrammar.docx");
```

### Ver también

* class [Document](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
