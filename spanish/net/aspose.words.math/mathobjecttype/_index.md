---
title: MathObjectType Enum
linktitle: MathObjectType
articleTitle: MathObjectType
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words.Math.MathObjectType para identificar y administrar fácilmente los tipos de objetos de Office Math para un mejor procesamiento de documentos.
type: docs
weight: 4800
url: /es/net/aspose.words.math/mathobjecttype/
---
## MathObjectType enumeration

Especifica el tipo de un objeto de Office Math.

```csharp
public enum MathObjectType
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| OMath | `0` | Instancia de texto matemático. |
| OMathPara | `1` | Párrafo de matemáticas, o zona de visualización de matemáticas, que contiene uno o másOMath elementos que están en modo visualización. |
| Accent | `2` | Función de acento, compuesta por una base y una marca diacrítica combinatoria. |
| Bar | `3` | Función de barra, que consta de un argumento base y una barra superior o inferior. |
| BorderBox | `4` | Objeto de cuadro de borde, que consiste en un borde dibujado alrededor de una instancia de texto matemático (como una fórmula o ecuación) |
| Box | `5` | Objeto de cuadro, que se utiliza para agrupar componentes de una ecuación u otra instancia de texto matemático. |
| Delimiter | `6` | Objeto delimitador, que consta de delimitadores de apertura y cierre (como paréntesis, llaves, corchetes y barras verticales) y un elemento contenido en su interior. |
| Degree | `7` | Grado en el radical matemático. |
| Argument | `8` | Objeto de argumento. Encierra entidades de Office Math cuando se usan como argumentos para otras entidades de Office Math. |
| Array | `9` | Objeto de matriz, que consta de una o más ecuaciones, expresiones u otras secuencias de texto matemático que se pueden justificar verticalmente como una unidad con respecto al texto circundante en la línea. |
| Fraction | `10` | Objeto de fracción, que consta de un numerador y un denominador separados por una barra de fracción. |
| Denominator | `11` | Denominador de un objeto fraccionario. |
| Numerator | `12` | Numerador del objeto Fracción. |
| Function | `13` | Objeto Función-Aplicar, que consta de un nombre de función y un elemento de argumento sobre el que se actúa. |
| FunctionName | `14` | Nombre de la función. Por ejemplo, los nombres de función son seno y coseno. |
| GroupCharacter | `15` | Objeto de grupo-carácter, que consiste en un carácter dibujado encima o debajo del texto, a menudo con el propósito de agrupar elementos visualmente |
| Limit | `16` | Límite inferior de laLowerLimit objeto y el límite superior de laUpperLimit función. |
| LowerLimit | `17` | Objeto de límite inferior, que consta de texto en la línea base y texto de tamaño reducido inmediatamente debajo de él. |
| UpperLimit | `18` | Objeto de límite superior, que consta de texto en la línea base y texto de tamaño reducido inmediatamente encima de él. |
| Matrix | `19` | Objeto de matriz, que consta de uno o más elementos dispuestos en una o más filas y una o más columnas. |
| MatrixRow | `20` | Fila única de la matriz. |
| NAry | `21` | Objeto n-ario, que consta de un objeto n-ario, una base (u operando) y límites superior e inferior opcionales. |
| Phantom | `22` | Objeto fantasma. |
| Radical | `23` | Objeto radical, que consta de un radical, un elemento base y un grado opcional. |
| SubscriptPart | `24` | Subíndice del objeto que puede tener parte subíndice. |
| SuperscriptPart | `25` | Superíndice del objeto superíndice. |
| PreSubSuperscript | `26` | Objeto Pre-Sub-Superíndice, que consta de un elemento base y un subíndice y superíndice colocados a la izquierda de la base. |
| Subscript | `27` | Objeto subíndice, que consta de un elemento base y un script de tamaño reducido colocado debajo y a la derecha. |
| SubSuperscript | `28` | Objeto subsuperíndice, que consta de un elemento base, un script de tamaño reducido colocado debajo y a la derecha, y un script de tamaño reducido colocado arriba y a la derecha. |
| Supercript | `29` | Objeto superíndice, que consta de un elemento base y un script de tamaño reducido colocado encima y a la derecha. |

## Ejemplos

Muestra cómo imprimir la estructura de nodos de cada nodo de matemáticas de oficina en un documento.

```csharp
public void OfficeMathToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    OfficeMathStructurePrinter visitor = new OfficeMathStructurePrinter();

    // Cuando conseguimos que un nodo compuesto acepte un visitante de documento, el visitante visita el nodo que lo acepta,
    // y luego recorre todos los nodos secundarios en profundidad.
    //El visitante puede leer y modificar cada nodo visitado.
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
/// Recorre el árbol no binario de nodos secundarios de un nodo.
/// Crea un mapa en forma de cadena de todos los nodos OfficeMath encontrados y sus hijos.
/// </summary>
public class OfficeMathStructurePrinter : DocumentVisitor
{
    public OfficeMathStructurePrinter()
    {
        mBuilder = new StringBuilder();
        mVisitorIsInsideOfficeMath = false;
    }

    /// <summary>
    /// Obtiene el texto simple del documento que fue acumulado por el visitante.
    /// </summary>
    public string GetText()
    {
        return mBuilder.ToString();
    }

    /// <summary>
    /// Se llama cuando se encuentra un nodo Ejecutar en el documento.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        if (mVisitorIsInsideOfficeMath) IndentAndAppendLine("[Run] \"" + run.GetText() + "\"");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Se llama cuando se encuentra un nodo OfficeMath en el documento.
    /// </summary>
    public override VisitorAction VisitOfficeMathStart(OfficeMath officeMath)
    {
        IndentAndAppendLine("[OfficeMath start] Math object type: " + officeMath.MathObjectType);
        mDocTraversalDepth++;
        mVisitorIsInsideOfficeMath = true;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Se llama después de que se hayan visitado todos los nodos secundarios de un nodo OfficeMath.
    /// </summary>
    public override VisitorAction VisitOfficeMathEnd(OfficeMath officeMath)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[OfficeMath end]");
        mVisitorIsInsideOfficeMath = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Agrega una línea al StringBuilder y sangrala dependiendo de qué tan profundo se encuentre el visitante en el árbol del documento.
    /// </summary>
    /// <param name="texto"></param>
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
