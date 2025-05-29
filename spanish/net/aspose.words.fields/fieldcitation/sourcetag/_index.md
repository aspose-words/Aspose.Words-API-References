---
title: FieldCitation.SourceTag
linktitle: SourceTag
articleTitle: SourceTag
second_title: Aspose.Words para .NET
description: Descubra la propiedad FieldCitation SourceTag, administre y personalice fácilmente los elementos Tag para una inserción de datos fluida y una mayor precisión de la fuente.
type: docs
weight: 60
url: /es/net/aspose.words.fields/fieldcitation/sourcetag/
---
## FieldCitation.SourceTag property

Obtiene o establece un valor que coincide con el**Etiqueta** Valor del elemento de la fuente a insertar.

```csharp
public string SourceTag { get; set; }
```

## Ejemplos

Muestra cómo trabajar con los campos CITA y BIBLIOGRAFÍA.

```csharp
//Abrir un documento que contenga las fuentes bibliográficas que podemos encontrar en
// Microsoft Word vía Referencias -> Citas y bibliografía -> Administrar fuentes.
Document doc = new Document(MyDir + "Bibliography.docx");
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Text to be cited with one source.");

// Crea una cita con solo el número de página y el autor del libro referenciado.
FieldCitation fieldCitation = (FieldCitation)builder.InsertField(FieldType.FieldCitation, true);

// Nos referimos a las fuentes utilizando sus nombres de etiquetas.
fieldCitation.SourceTag = "Book1";
fieldCitation.PageNumber = "85";
fieldCitation.SuppressAuthor = false;
fieldCitation.SuppressTitle = true;
fieldCitation.SuppressYear = true;

Assert.AreEqual(" CITATION  Book1 \\p 85 \\t \\y", fieldCitation.GetFieldCode());

// Cree una cita más detallada que cite dos fuentes.
builder.InsertParagraph();
builder.Write("Text to be cited with two sources.");
fieldCitation = (FieldCitation)builder.InsertField(FieldType.FieldCitation, true);
fieldCitation.SourceTag = "Book1";
fieldCitation.AnotherSourceTag = "Book2";
fieldCitation.FormatLanguageId = "en-US";
fieldCitation.PageNumber = "19";
fieldCitation.Prefix = "Prefix ";
fieldCitation.Suffix = " Suffix";
fieldCitation.SuppressAuthor = false;
fieldCitation.SuppressTitle = false;
fieldCitation.SuppressYear = false;
fieldCitation.VolumeNumber = "VII";

Assert.AreEqual(" CITATION  Book1 \\m Book2 \\l en-US \\p 19 \\f \"Prefix \" \\s \" Suffix\" \\v VII", fieldCitation.GetFieldCode());

//Podemos utilizar un campo BIBLIOGRAFÍA para mostrar todas las fuentes dentro del documento.
builder.InsertBreak(BreakType.PageBreak);
FieldBibliography fieldBibliography = (FieldBibliography)builder.InsertField(FieldType.FieldBibliography, true);
fieldBibliography.FormatLanguageId = "5129";
fieldBibliography.FilterLanguageId = "5129";
fieldBibliography.SourceTag = "Book2";

Assert.AreEqual(" BIBLIOGRAPHY  \\l 5129 \\f 5129 \\m Book2", fieldBibliography.GetFieldCode());

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.CITATION.docx");
```

### Ver también

* class [FieldCitation](../)
* espacio de nombres [Aspose.Words.Fields](../../../aspose.words.fields/)
* asamblea [Aspose.Words](../../../)
