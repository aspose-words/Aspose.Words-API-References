---
title: Body.AcceptEnd
linktitle: AcceptEnd
articleTitle: AcceptEnd
second_title: Aspose.Words para .NET
description: Mejore su experiencia web con el método Body AcceptEnd, diseñado para aceptar sin problemas a los visitantes al final del documento para una mejor navegación.
type: docs
weight: 50
url: /es/net/aspose.words/body/acceptend/
---
## Body.AcceptEnd method

Acepta que un visitante visite el final del cuerpo del documento.

```csharp
public override VisitorAction AcceptEnd(DocumentVisitor visitor)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| visitor | DocumentVisitor | El visitante del documento. |

### Valor_devuelto

La acción que debe realizar el visitante.

## Ejemplos

Muestra cómo procesar caracteres de tabulación de posición absoluta con un visitante de documento.

```csharp
public void DocumentToTxt()
{
    Document doc = new Document(MyDir + "Absolute position tab.docx");

    // Extraiga el contenido de texto de nuestro documento aceptando este visitante de documento personalizado.
    DocTextExtractor myDocTextExtractor = new DocTextExtractor();
    Section fisrtSection = doc.FirstSection;
    fisrtSection.Body.Accept(myDocTextExtractor);
    // Visita solo el inicio del cuerpo del documento.
    fisrtSection.Body.AcceptStart(myDocTextExtractor);
    // Visita solo el final del cuerpo del documento.
    fisrtSection.Body.AcceptEnd(myDocTextExtractor);

    // La posición absoluta de tabulación, que no tiene equivalente en formato de cadena, se ha convertido explícitamente en un carácter de tabulación.
    Assert.AreEqual("Before AbsolutePositionTab\tAfter AbsolutePositionTab", myDocTextExtractor.GetText());

    // Un AbsolutePositionTab también puede aceptar un DocumentVisitor por sí solo.
    AbsolutePositionTab absPositionTab = (AbsolutePositionTab)doc.FirstSection.Body.FirstParagraph.GetChild(NodeType.SpecialChar, 0, true);

    myDocTextExtractor = new DocTextExtractor();
    absPositionTab.Accept(myDocTextExtractor);

    Assert.AreEqual("\t", myDocTextExtractor.GetText());
}

/// <summary>
Recopila el contenido textual de todas las ejecuciones del documento visitado. Reemplaza todos los caracteres de tabulación absolutos por tabulaciones normales.
/// </summary>
public class DocTextExtractor : DocumentVisitor
{
    public DocTextExtractor()
    {
        mBuilder = new StringBuilder();
    }

    /// <summary>
    /// Se llama cuando se encuentra un nodo Ejecutar en el documento.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        AppendText(run.Text);
        return VisitorAction.Continue;
    }

    /// <summary>
    /// Se llama cuando se encuentra un nodo AbsolutePositionTab en el documento.
    /// </summary>
    public override VisitorAction VisitAbsolutePositionTab(AbsolutePositionTab tab)
    {
        mBuilder.Append("\t");
        return VisitorAction.Continue;
    }

    /// <summary>
    /// Agrega texto a la salida actual. Respeta el indicador de salida habilitada o deshabilitada.
    /// </summary>
    private void AppendText(string text)
    {
        mBuilder.Append(text);
    }

    /// <summary>
    /// Texto plano del documento que fue acumulado por el visitante.
    /// </summary>
    public string GetText()
    {
        return mBuilder.ToString();
    }

    private readonly StringBuilder mBuilder;
}
```

### Ver también

* enum [VisitorAction](../../visitoraction/)
* class [DocumentVisitor](../../documentvisitor/)
* class [Body](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
