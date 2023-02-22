---
title: AbsolutePositionTab.Accept
second_title: Referencia de API de Aspose.Words para .NET
description: AbsolutePositionTab método. Acepta un visitante.
type: docs
weight: 10
url: /es/net/aspose.words/absolutepositiontab/accept/
---
## AbsolutePositionTab.Accept method

Acepta un visitante.

```csharp
public override bool Accept(DocumentVisitor visitor)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| visitor | DocumentVisitor | El visitante que visitará el nodo. |

### Valor_devuelto

Falso si el visitante solicitó que se detuviera la enumeración.

### Observaciones

Llama a DocumentVisitor.VisitAbsolutePositionTab.

Para obtener más información, consulte el patrón de diseño Visitante.

### Ejemplos

Muestra cómo procesar caracteres de tabulación de posición absoluta con un visitante del documento.

```csharp
public void DocumentToTxt()
{
    Document doc = new Document(MyDir + "Absolute position tab.docx");

    // Extraiga el contenido de texto de nuestro documento aceptando este visitante de documento personalizado.
    DocTextExtractor myDocTextExtractor = new DocTextExtractor();
    doc.FirstSection.Body.Accept(myDocTextExtractor);

    // La tabulación de posición absoluta, que no tiene equivalente en forma de cadena, se ha convertido explícitamente en un carácter de tabulación.
    Assert.AreEqual("Before AbsolutePositionTab\tAfter AbsolutePositionTab", myDocTextExtractor.GetText());

    // Una AbsolutePositionTab también puede aceptar un DocumentVisitor por sí misma.
    AbsolutePositionTab absPositionTab = (AbsolutePositionTab)doc.FirstSection.Body.FirstParagraph.GetChild(NodeType.SpecialChar, 0, true);

    myDocTextExtractor = new DocTextExtractor();
    absPositionTab.Accept(myDocTextExtractor);

    Assert.AreEqual("\t", myDocTextExtractor.GetText());
}

/// <summary>
/// Recopila el contenido de texto de todas las ejecuciones en el documento visitado. Reemplaza todos los caracteres de tabulación absolutos con tabulaciones ordinarias.
/// </summary>
public class DocTextExtractor : DocumentVisitor
{
    public DocTextExtractor()
    {
        mBuilder = new StringBuilder();
    }

    /// <summary>
    /// Llamado cuando se encuentra un nodo Ejecutar en el documento.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        AppendText(run.Text);
        return VisitorAction.Continue;
    }

    /// <summary>
    /// Llamado cuando se encuentra un nodo AbsolutePositionTab en el documento.
    /// </summary>
    public override VisitorAction VisitAbsolutePositionTab(AbsolutePositionTab tab)
    {
        mBuilder.Append("\t");
        return VisitorAction.Continue;
    }

    /// <summary>
    /// Agrega texto a la salida actual. Respeta el indicador de salida activado/desactivado.
    /// </summary>
    private void AppendText(string text)
    {
        mBuilder.Append(text);
    }

    /// <summary>
    /// Texto sin formato del documento que fue acumulado por el visitante.
    /// </summary>
    public string GetText()
    {
        return mBuilder.ToString();
    }

    private readonly StringBuilder mBuilder;
}
```

### Ver también

* class [DocumentVisitor](../../documentvisitor/)
* class [AbsolutePositionTab](../)
* espacio de nombres [Aspose.Words](../../absolutepositiontab/)
* asamblea [Aspose.Words](../../../)


