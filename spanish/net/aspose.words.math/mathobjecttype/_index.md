---
title: MathObjectType
second_title: Referencia de API de Aspose.Words para .NET
description: Especifica el tipo de un objeto Office Math.
type: docs
weight: 3870
url: /es/net/aspose.words.math/mathobjecttype/
---
## MathObjectType enumeration

Especifica el tipo de un objeto Office Math.

```csharp
public enum MathObjectType
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| OMath | `0` | Instancia de texto matemático. |
| OMathPara | `1` | Párrafo matemático, o zona matemática de visualización, que contiene uno o másOMath elementos que están en modo de visualización. |
| Accent | `2` | Función de acento, que consta de una base y un signo diacrítico combinado. |
| Bar | `3` | Función de barra, que consta de un argumento base y una barra superior o inferior. |
| BorderBox | `4` | Objeto de cuadro de borde, que consiste en un borde dibujado alrededor de una instancia de texto matemático (como una fórmula o ecuación) |
| Box | `5` | Objeto de cuadro, que se utiliza para agrupar componentes de una ecuación u otra instancia de texto matemático. |
| Delimiter | `6` | Objeto delimitador, que consta de delimitadores de apertura y cierre (como paréntesis, llaves, corchetes y barras verticales) y un elemento contenido dentro. |
| Degree | `7` | Grado en el radical matemático. |
| Argument | `8` | Objeto de argumento. Incluye entidades de Office Math cuando se utilizan como argumentos para otras entidades de Office Math. |
| Array | `9` | Objeto de matriz, que consta de una o más ecuaciones, expresiones u otras secuencias de texto matemático que se pueden justificar verticalmente como una unidad con respecto al texto circundante en la línea. |
| Fraction | `10` | Objeto fracción, formado por un numerador y un denominador separados por una barra fraccionaria. |
| Denominator | `11` | Denominador de un objeto fracción. |
| Numerator | `12` | Numerador del objeto Fracción. |
| Function | `13` | Objeto Function-Apply, que consiste en un nombre de función y un elemento de argumento sobre el que se actúa. |
| FunctionName | `14` | Nombre de la función. Por ejemplo, los nombres de las funciones son sin y cos. |
| GroupCharacter | `15` | Objeto Group-Character, que consta de un carácter dibujado encima o debajo del texto, a menudo con el propósito de agrupar elementos visualmente |
| Limit | `16` | Límite inferior delLowerLimit objeto y el límite superior delUpperLimit función. |
| LowerLimit | `17` | Objeto de límite inferior, que consta de texto en la línea de base y texto de tamaño reducido inmediatamente debajo. |
| UpperLimit | `18` | Objeto de límite superior, que consta de texto en la línea de base y texto de tamaño reducido inmediatamente encima. |
| Matrix | `19` | Objeto matriz, formado por uno o más elementos dispuestos en una o más filas y una o más columnas. |
| MatrixRow | `20` | Fila única de la matriz. |
| NAry | `21` | Objeto n-ario, que consta de un objeto n-ario, una base (u operando) y límites superior e inferior opcionales. |
| Phantom | `22` | Objeto fantasma. |
| Radical | `23` | Objeto radical, formado por un radical, un elemento base y un grado opcional . |
| SubscriptPart | `24` | Subíndice del objeto que puede tener parte de subíndice. |
| SuperscriptPart | `25` | Superíndice del objeto superíndice. |
| PreSubSuperscript | `26` | Objeto Pre-Sub-Superíndice, que consta de un elemento base y un subíndice y un superíndice colocados a la izquierda de la base. |
| Subscript | `27` | Objeto subíndice, que consta de un elemento base y un guión de tamaño reducido colocado debajo y a la derecha. |
| SubSuperscript | `28` | Objeto subsuperíndice, que consta de un elemento base, un guión de tamaño reducido colocado debajo ya la derecha y un guión de tamaño reducido colocado arriba ya la derecha. |
| Supercript | `29` | Objeto superíndice, que consta de un elemento base y un guión de tamaño reducido colocado arriba y a la derecha. |

### Ejemplos

Muestra cómo imprimir la estructura de nodos de cada nodo matemático de oficina en un documento.

```csharp
public void OfficeMathToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    OfficeMathStructurePrinter visitor = new OfficeMathStructurePrinter();

    // Cuando conseguimos que un nodo compuesto acepte un documento visitante, el visitante visita el nodo de aceptación,
    // y luego atraviesa todos los elementos secundarios del nodo en profundidad.
    // El visitante puede leer y modificar cada nodo visitado.
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
/// Atraviesa el árbol no binario de nodos secundarios de un nodo.
/// Crea un mapa en forma de cadena de todos los nodos de OfficeMath encontrados y sus hijos.
/// </summary>
public class OfficeMathStructurePrinter : DocumentVisitor
{
    public OfficeMathStructurePrinter()
    {
        mBuilder = new StringBuilder();
        mVisitorIsInsideOfficeMath = false;
    }

    /// <summary>
    /// Obtiene el texto sin formato del documento que fue acumulado por el visitante.
    /// </summary>
    public string GetText()
    {
        return mBuilder.ToString();
    }

    /// <summary>
    /// Llamado cuando se encuentra un nodo Ejecutar en el documento.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        if (mVisitorIsInsideOfficeMath) IndentAndAppendLine("[Run] \"" + run.GetText() + "\"");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Llamado cuando se encuentra un nodo OfficeMath en el documento.
    /// </summary>
    public override VisitorAction VisitOfficeMathStart(OfficeMath officeMath)
    {
        IndentAndAppendLine("[OfficeMath start] Math object type: " + officeMath.MathObjectType);
        mDocTraversalDepth++;
        mVisitorIsInsideOfficeMath = true;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Llamado después de que se hayan visitado todos los nodos secundarios de un nodo OfficeMath.
    /// </summary>
    public override VisitorAction VisitOfficeMathEnd(OfficeMath officeMath)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[OfficeMath end]");
        mVisitorIsInsideOfficeMath = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Agregue una línea al StringBuilder y sangre dependiendo de qué tan profundo esté el visitante en el árbol del documento.
    /// </summary>
    /// <parámetro nombre="texto"></parámetro>
    private void IndentAndAppendLine(string text)
    {
        for (int i = 0; i < mDocTraversalDepth; i++) mBuilder.Append("|  ");

        mBuilder.AppendLine(text);
    }

    private bool mVisitorIsInsideOfficeMath;
    private int mDocTraversalDepth;
    private readonly StringBuilder mBuilder;
}
```

### Ver también

* espacio de nombres [Aspose.Words.Math](../../aspose.words.math/)
* asamblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
