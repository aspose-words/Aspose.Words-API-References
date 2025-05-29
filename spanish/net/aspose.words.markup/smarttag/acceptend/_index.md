---
title: SmartTag.AcceptEnd
linktitle: AcceptEnd
articleTitle: AcceptEnd
second_title: Aspose.Words para .NET
description: Descubra cómo el método SmartTag AcceptEnd mejora la interacción de los visitantes al gestionar fácilmente las experiencias de fin de visita. ¡Impulse la interacción en su sitio web hoy mismo!
type: docs
weight: 70
url: /es/net/aspose.words.markup/smarttag/acceptend/
---
## SmartTag.AcceptEnd method

Acepta un visitante por visitar el final de la SmartTag.

```csharp
public override VisitorAction AcceptEnd(DocumentVisitor visitor)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| visitor | DocumentVisitor | El visitante del documento. |

### Valor_devuelto

La acción que debe realizar el visitante.

## Ejemplos

Muestra cómo crear etiquetas inteligentes.

```csharp
public void Create()
{
    Document doc = new Document();

    // Una etiqueta inteligente aparece en un documento con Microsoft Word y reconoce una parte de su texto como algún tipo de datos,
    // como un nombre, una fecha o una dirección, y lo convierte en un hipervínculo que muestra un subrayado punteado de color púrpura.
    SmartTag smartTag = new SmartTag(doc);

    // Las etiquetas inteligentes son nodos compuestos que contienen el texto reconocido en su totalidad.
    // Agregue contenido a esta etiqueta inteligente manualmente.
    smartTag.AppendChild(new Run(doc, "May 29, 2019"));

    //Microsoft Word puede reconocer el contenido anterior como una fecha.
    // Las etiquetas inteligentes utilizan la propiedad "Elemento" para reflejar el tipo de datos que contienen.
    smartTag.Element = "date";

    // Algunos tipos de etiquetas inteligentes procesan sus contenidos y los convierten en propiedades XML personalizadas.
    smartTag.Properties.Add(new CustomXmlProperty("Day", string.Empty, "29"));
    smartTag.Properties.Add(new CustomXmlProperty("Month", string.Empty, "5"));
    smartTag.Properties.Add(new CustomXmlProperty("Year", string.Empty, "2019"));

    // Establezca el URI de la etiqueta inteligente en el valor predeterminado.
    smartTag.Uri = "urn:schemas-microsoft-com:office:smarttags";

    doc.FirstSection.Body.FirstParagraph.AppendChild(smartTag);
    doc.FirstSection.Body.FirstParagraph.AppendChild(new Run(doc, " is a date. "));

    // Crea otra etiqueta inteligente para un símbolo de bolsa.
    smartTag = new SmartTag(doc);
    smartTag.Element = "stockticker";
    smartTag.Uri = "urn:schemas-microsoft-com:office:smarttags";

    smartTag.AppendChild(new Run(doc, "MSFT"));

    doc.FirstSection.Body.FirstParagraph.AppendChild(smartTag);
    doc.FirstSection.Body.FirstParagraph.AppendChild(new Run(doc, " is a stock ticker."));

    // Imprima todas las etiquetas inteligentes en nuestro documento usando un visitante de documentos.
    doc.Accept(new SmartTagPrinter());

    // Las versiones anteriores de Microsoft Word admiten etiquetas inteligentes.
    doc.Save(ArtifactsDir + "SmartTag.Create.doc");

    // Utilice el método "RemoveSmartTags" para eliminar todas las etiquetas inteligentes de un documento.
    Assert.AreEqual(2, doc.GetChildNodes(NodeType.SmartTag, true).Count);

    doc.RemoveSmartTags();

    Assert.AreEqual(0, doc.GetChildNodes(NodeType.SmartTag, true).Count);
}

/// <summary>
/// Imprime las etiquetas inteligentes visitadas y su contenido.
/// </summary>
private class SmartTagPrinter : DocumentVisitor
{
    /// <summary>
    /// Se llama cuando se encuentra un nodo SmartTag en el documento.
    /// </summary>
    public override VisitorAction VisitSmartTagStart(SmartTag smartTag)
    {
        Console.WriteLine($"Smart tag type: {smartTag.Element}");
        return VisitorAction.Continue;
    }

    /// <summary>
    /// Se llama cuando finaliza la visita a un nodo SmartTag.
    /// </summary>
    public override VisitorAction VisitSmartTagEnd(SmartTag smartTag)
    {
        Console.WriteLine($"\tContents: \"{smartTag.ToString(SaveFormat.Text)}\"");

        if (smartTag.Properties.Count == 0)
        {
            Console.WriteLine("\tContains no properties");
        }
        else
        {
            Console.Write("\tProperties: ");
            string[] properties = new string[smartTag.Properties.Count];
            int index = 0;

            foreach (CustomXmlProperty cxp in smartTag.Properties)
                properties[index++] = $"\"{cxp.Name}\" = \"{cxp.Value}\"";

            Console.WriteLine(string.Join(", ", properties));
        }

        return VisitorAction.Continue;
    }
}
```

### Ver también

* enum [VisitorAction](../../../aspose.words/visitoraction/)
* class [DocumentVisitor](../../../aspose.words/documentvisitor/)
* class [SmartTag](../)
* espacio de nombres [Aspose.Words.Markup](../../../aspose.words.markup/)
* asamblea [Aspose.Words](../../../)
