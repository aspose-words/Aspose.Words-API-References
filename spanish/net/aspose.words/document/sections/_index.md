---
title: Document.Sections
second_title: Referencia de API de Aspose.Words para .NET
description: Document propiedad. Devuelve una colección que representa todas las secciones del documento.
type: docs
weight: 350
url: /es/net/aspose.words/document/sections/
---
## Document.Sections property

Devuelve una colección que representa todas las secciones del documento.

```csharp
public SectionCollection Sections { get; }
```

### Ejemplos

Muestra cómo agregar y eliminar secciones en un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Section 1");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Section 2");

Assert.AreEqual("Section 1\x000cSection 2", doc.GetText().Trim());

// Eliminar la primera sección del documento.
doc.Sections.RemoveAt(0);

Assert.AreEqual("Section 2", doc.GetText().Trim());

// Agregue una copia de lo que ahora es la primera sección al final del documento.
int lastSectionIdx = doc.Sections.Count - 1;
Section newSection = doc.Sections[lastSectionIdx].Clone();
doc.Sections.Add(newSection);

Assert.AreEqual("Section 2\x000cSection 2", doc.GetText().Trim());
```

Muestra cómo especificar cómo una nueva sección se separa de la anterior.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("This text is in section 1.");

// Los tipos de salto de sección determinan cómo una nueva sección se separa de la sección anterior.
// A continuación se muestran cinco tipos de saltos de sección.
// 1 - Comienza la siguiente sección en una nueva página:
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Writeln("This text is in section 2.");

Assert.AreEqual(SectionStart.NewPage, doc.Sections[1].PageSetup.SectionStart);

// 2 - Comienza la siguiente sección en la página actual:
builder.InsertBreak(BreakType.SectionBreakContinuous);
builder.Writeln("This text is in section 3.");

Assert.AreEqual(SectionStart.Continuous, doc.Sections[2].PageSetup.SectionStart);

// 3 - Comienza la siguiente sección en una nueva página par:
builder.InsertBreak(BreakType.SectionBreakEvenPage);
builder.Writeln("This text is in section 4.");

Assert.AreEqual(SectionStart.EvenPage, doc.Sections[3].PageSetup.SectionStart);

// 4 - Comienza la siguiente sección en una nueva página impar:
builder.InsertBreak(BreakType.SectionBreakOddPage);
builder.Writeln("This text is in section 5.");

Assert.AreEqual(SectionStart.OddPage, doc.Sections[4].PageSetup.SectionStart);

// 5 - Comienza la siguiente sección en una nueva columna:
TextColumnCollection columns = builder.PageSetup.TextColumns;
columns.SetCount(2);

builder.InsertBreak(BreakType.SectionBreakNewColumn);
builder.Writeln("This text is in section 6.");

Assert.AreEqual(SectionStart.NewColumn, doc.Sections[5].PageSetup.SectionStart);

doc.Save(ArtifactsDir + "PageSetup.SetSectionStart.docx");
```

### Ver también

* class [SectionCollection](../../sectioncollection/)
* class [Document](../)
* espacio de nombres [Aspose.Words](../../document/)
* asamblea [Aspose.Words](../../../)


