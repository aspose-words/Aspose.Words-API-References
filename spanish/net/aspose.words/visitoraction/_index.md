---
title: VisitorAction Enum
linktitle: VisitorAction
articleTitle: VisitorAction
second_title: Aspose.Words para .NET
description: Explore la enumeración Aspose.Words.VisitorAction para administrar sin esfuerzo la enumeración de nodos, mejorando la eficiencia y el control del procesamiento de sus documentos.
type: docs
weight: 7470
url: /es/net/aspose.words/visitoraction/
---
## VisitorAction enumeration

Permite al visitante controlar la enumeración de nodos.

```csharp
public enum VisitorAction
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Continue | `0` | El visitante solicita que la enumeración continúe. |
| SkipThisNode | `1` | El visitante solicita omitir el nodo actual y continuar con la enumeración. |
| Stop | `2` | El visitante solicita que se detenga la enumeración de nodos. |

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

* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)
