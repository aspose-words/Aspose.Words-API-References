---
title: Body.ParentSection
second_title: Referencia de API de Aspose.Words para .NET
description: Body propiedad. Obtiene la sección principal de esta historia.
type: docs
weight: 30
url: /es/net/aspose.words/body/parentsection/
---
## Body.ParentSection property

Obtiene la sección principal de esta historia.

```csharp
public Section ParentSection { get; }
```

### Observaciones

`ParentSection` es equivalente a[`ParentNode`](../../node/parentnode/) lanzado a[`Section`](../../section/).

### Ejemplos

Muestra cómo almacenar notas finales al final de cada sección y modificar sus posiciones.

```csharp
public void SuppressEndnotes()
{
    Document doc = new Document();
    doc.RemoveAllChildren();

     // De forma predeterminada, un documento compila todas las notas finales al final.
    Assert.AreEqual(EndnotePosition.EndOfDocument, doc.EndnoteOptions.Position);

    // Usamos la propiedad "Position" del objeto "EndnoteOptions" del documento
     // para recopilar notas finales al final de cada sección.
    doc.EndnoteOptions.Position = EndnotePosition.EndOfSection;

    InsertSectionWithEndnote(doc, "Section 1", "Endnote 1, will stay in section 1");
    InsertSectionWithEndnote(doc, "Section 2", "Endnote 2, will be pushed down to section 3");
    InsertSectionWithEndnote(doc, "Section 3", "Endnote 3, will stay in section 3");

    // Mientras hacemos que las secciones muestren sus respectivas notas finales, podemos configurar el indicador "SuppressEndnotes"
    // del objeto "PageSetup" de una sección a "true" para volver al comportamiento predeterminado y pasar sus notas finales
    // a la siguiente sección.
    PageSetup pageSetup = doc.Sections[1].PageSetup;
    pageSetup.SuppressEndnotes = true;

    doc.Save(ArtifactsDir + "PageSetup.SuppressEndnotes.docx");
}

/// <summary>
/// Agregar una sección con texto y una nota final a un documento.
/// </summary>
private static void InsertSectionWithEndnote(Document doc, string sectionBodyText, string endnoteText)
{
    Section section = new Section(doc);

    doc.AppendChild(section);

    Body body = new Body(doc);
    section.AppendChild(body);

    Assert.AreEqual(section, body.ParentNode);

    Paragraph para = new Paragraph(doc);
    body.AppendChild(para);

    Assert.AreEqual(body, para.ParentNode);

    DocumentBuilder builder = new DocumentBuilder(doc);
    builder.MoveTo(para);
    builder.Write(sectionBodyText);
    builder.InsertFootnote(FootnoteType.Endnote, endnoteText);
}
```

### Ver también

* class [Section](../../section/)
* class [Body](../)
* espacio de nombres [Aspose.Words](../../body/)
* asamblea [Aspose.Words](../../../)


