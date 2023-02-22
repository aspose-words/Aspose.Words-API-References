---
title: SmartTag.SmartTag
second_title: Referencia de API de Aspose.Words para .NET
description: SmartTag constructor. Inicializa una nueva instancia delSmartTag clase.
type: docs
weight: 10
url: /es/net/aspose.words.markup/smarttag/smarttag/
---
## SmartTag constructor

Inicializa una nueva instancia del[`SmartTag`](../) clase.

```csharp
public SmartTag(DocumentBase doc)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| doc | DocumentBase | El documento del propietario. |

### Observaciones

Cuando crea un nuevo nodo, debe especificar un documento al que pertenece el nodo. Un nodo no puede existir sin un documento porque depende de las estructuras de todo el documento como listas y estilos. Aunque un nodo siempre pertenece a un documento, un nodo puede o no ser parte del árbol del documento.

Cuando se crea un nodo, pertenece a un documento, pero aún no forma parte del documento tree y[`ParentNode`](../../../aspose.words/node/parentnode/) es nulo. Para insertar un nodo en el documento, use the [`InsertAfter`](../../../aspose.words/compositenode/insertafter/) o[`InsertBefore`](../../../aspose.words/compositenode/insertbefore/) métodos en el nodo principal.

### Ejemplos

Muestra cómo crear etiquetas inteligentes.

```csharp
public void Create()
{
    Document doc = new Document();

    // Aparece una etiqueta inteligente en un documento con Microsoft Word que reconoce una parte de su texto como algún tipo de datos,
    // como un nombre, fecha o dirección, y lo convierte en un hipervínculo que muestra un subrayado punteado de color púrpura.
    SmartTag smartTag = new SmartTag(doc);

    // Las etiquetas inteligentes son nodos compuestos que contienen su texto reconocido en su totalidad.
    // Agregue contenido a esta etiqueta inteligente manualmente.
    smartTag.AppendChild(new Run(doc, "May 29, 2019"));

    // Microsoft Word puede reconocer el contenido anterior como una fecha.
    // Las etiquetas inteligentes utilizan la propiedad "Elemento" para reflejar el tipo de datos que contienen.
    smartTag.Element = "date";

    // Algunos tipos de etiquetas inteligentes procesan aún más su contenido en propiedades XML personalizadas.
    smartTag.Properties.Add(new CustomXmlProperty("Day", string.Empty, "29"));
    smartTag.Properties.Add(new CustomXmlProperty("Month", string.Empty, "5"));
    smartTag.Properties.Add(new CustomXmlProperty("Year", string.Empty, "2019"));

    // Establecer el URI de la etiqueta inteligente en el valor predeterminado.
    smartTag.Uri = "urn:schemas-microsoft-com:office:smarttags";

    doc.FirstSection.Body.FirstParagraph.AppendChild(smartTag);
    doc.FirstSection.Body.FirstParagraph.AppendChild(new Run(doc, " is a date. "));

    // Cree otra etiqueta inteligente para un tablero de cotizaciones.
    smartTag = new SmartTag(doc);
    smartTag.Element = "stockticker";
    smartTag.Uri = "urn:schemas-microsoft-com:office:smarttags";

    smartTag.AppendChild(new Run(doc, "MSFT"));

    doc.FirstSection.Body.FirstParagraph.AppendChild(smartTag);
    doc.FirstSection.Body.FirstParagraph.AppendChild(new Run(doc, " is a stock ticker."));

    // Imprime todas las etiquetas inteligentes en nuestro documento usando un visitante del documento.
    doc.Accept(new SmartTagPrinter());

    // Las versiones anteriores de Microsoft Word admiten etiquetas inteligentes.
    doc.Save(ArtifactsDir + "SmartTag.Create.doc");

    // Use el método "RemoveSmartTags" para eliminar todas las etiquetas inteligentes de un documento.
    Assert.AreEqual(2, doc.GetChildNodes(NodeType.SmartTag, true).Count);

    doc.RemoveSmartTags();

    Assert.AreEqual(0, doc.GetChildNodes(NodeType.SmartTag, true).Count);
}

/// <summary>
/// Imprime las etiquetas inteligentes visitadas y sus contenidos.
/// </summary>
private class SmartTagPrinter : DocumentVisitor
{
    /// <summary>
    /// Llamado cuando se encuentra un nodo SmartTag en el documento.
    /// </summary>
    public override VisitorAction VisitSmartTagStart(SmartTag smartTag)
    {
        Console.WriteLine($"Smart tag type: {smartTag.Element}");
        return VisitorAction.Continue;
    }

    /// <summary>
    /// Llamado cuando finaliza la visita de un nodo SmartTag.
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

* class [DocumentBase](../../../aspose.words/documentbase/)
* class [SmartTag](../)
* espacio de nombres [Aspose.Words.Markup](../../smarttag/)
* asamblea [Aspose.Words](../../../)


