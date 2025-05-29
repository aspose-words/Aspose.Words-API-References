---
title: PageSetup.SuppressEndnotes
linktitle: SuppressEndnotes
articleTitle: SuppressEndnotes
second_title: Aspose.Words para .NET
description: Descubra cómo la propiedad SuppressEndnotes de PageSetup mejora el diseño de su documento al controlar la ubicación de las notas finales para lograr secciones más claras y organizadas.
type: docs
weight: 410
url: /es/net/aspose.words/pagesetup/suppressendnotes/
---
## PageSetup.SuppressEndnotes property

Verdadero si las notas finales se imprimen al final de la siguiente sección que no las suprime. Las notas finales suprimidas se imprimen antes de las notas finales de esa sección.

```csharp
public bool SuppressEndnotes { get; set; }
```

## Ejemplos

Muestra cómo almacenar notas finales al final de cada sección y modificar sus posiciones.

```csharp
public void SuppressEndnotes()
{
    Document doc = new Document();
    doc.RemoveAllChildren();

     // De forma predeterminada, un documento compila todas las notas finales al final.
    Assert.AreEqual(EndnotePosition.EndOfDocument, doc.EndnoteOptions.Position);

    // Utilizamos la propiedad "Posición" del objeto "EndnoteOptions" del documento
     // para recopilar notas finales al final de cada sección.
    doc.EndnoteOptions.Position = EndnotePosition.EndOfSection;

    InsertSectionWithEndnote(doc, "Section 1", "Endnote 1, will stay in section 1");
    InsertSectionWithEndnote(doc, "Section 2", "Endnote 2, will be pushed down to section 3");
    InsertSectionWithEndnote(doc, "Section 3", "Endnote 3, will stay in section 3");

    // Mientras hacemos que las secciones muestren sus respectivas notas finales, podemos configurar el indicador "Suprimir notas finales"
    // del objeto "PageSetup" de una sección a "verdadero" para volver al comportamiento predeterminado y pasar sus notas finales
    //pasamos a la siguiente sección.
    PageSetup pageSetup = doc.Sections[1].PageSetup;
    pageSetup.SuppressEndnotes = true;

    doc.Save(ArtifactsDir + "PageSetup.SuppressEndnotes.docx");
}

/// <summary>
/// Añade una sección con texto y una nota final a un documento.
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

* class [PageSetup](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
