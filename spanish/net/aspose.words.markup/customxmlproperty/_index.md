---
title: CustomXmlProperty
second_title: Referencia de API de Aspose.Words para .NET
description: Representa un solo atributo XML personalizado o una propiedad de etiqueta inteligente.
type: docs
weight: 3700
url: /es/net/aspose.words.markup/customxmlproperty/
---
## CustomXmlProperty class

Representa un solo atributo XML personalizado o una propiedad de etiqueta inteligente.

```csharp
public class CustomXmlProperty
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [CustomXmlProperty](customxmlproperty)(string, string, string) | Inicializa una nueva instancia de esta clase. |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Name](../../aspose.words.markup/customxmlproperty/name) { get; } | Especifica el nombre del atributo XML personalizado o propiedad de etiqueta inteligente. |
| [Uri](../../aspose.words.markup/customxmlproperty/uri) { get; set; } | Obtiene o establece el URI del espacio de nombres del atributo XML personalizado o la propiedad de la etiqueta inteligente. |
| [Value](../../aspose.words.markup/customxmlproperty/value) { get; set; } | Obtiene o establece el valor del atributo XML personalizado o la propiedad de la etiqueta inteligente. |

### Observaciones

Se utiliza como elemento de un[`CustomXmlPropertyCollection`](../customxmlpropertycollection) recopilación.

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

* espacio de nombres [Aspose.Words.Markup](../../aspose.words.markup)
* asamblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
