---
title: FieldStart
second_title: Referencia de API de Aspose.Words para .NET
description: Representa el inicio de un campo de Word en un documento.
type: docs
weight: 2280
url: /es/net/aspose.words.fields/fieldstart/
---
## FieldStart class

Representa el inicio de un campo de Word en un documento.

```csharp
public class FieldStart : FieldChar
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Especifica el identificador de nodo personalizado. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Obtiene el documento al que pertenece este nodo. |
| [FieldData](../../aspose.words.fields/fieldstart/fielddata/) { get; } | Obtiene datos de campos personalizados asociados con el campo. |
| [FieldType](../../aspose.words.fields/fieldchar/fieldtype/) { get; } | Devuelve el tipo del campo. |
| [Font](../../aspose.words/inline/font/) { get; } | Proporciona acceso al formato de fuente de este objeto. |
| virtual [IsComposite](../../aspose.words/node/iscomposite/) { get; } | Devuelve verdadero si este nodo puede contener otros nodos. |
| [IsDeleteRevision](../../aspose.words/inline/isdeleterevision/) { get; } | Devuelve verdadero si este objeto se eliminó en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [IsDirty](../../aspose.words.fields/fieldchar/isdirty/) { get; set; } | Obtiene o establece si el resultado actual del campo ya no es correcto (obsoleto) debido a otras modificaciones realizadas en el documento. |
| [IsFormatRevision](../../aspose.words/inline/isformatrevision/) { get; } | Devuelve verdadero si se cambió el formato del objeto en Microsoft Word mientras estaba habilitado el seguimiento de cambios. |
| [IsInsertRevision](../../aspose.words/inline/isinsertrevision/) { get; } | Devuelve verdadero si este objeto se insertó en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [IsLocked](../../aspose.words.fields/fieldchar/islocked/) { get; set; } | Obtiene o establece si el campo principal está bloqueado (no debe recalcular su resultado). |
| [IsMoveFromRevision](../../aspose.words/inline/ismovefromrevision/) { get; } | Devoluciones **verdadero** si este objeto se movió (eliminó) en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [IsMoveToRevision](../../aspose.words/inline/ismovetorevision/) { get; } | Devoluciones **verdadero** si este objeto se movió (insertó) en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Obtiene el nodo que sigue inmediatamente a este nodo. |
| override [NodeType](../../aspose.words.fields/fieldstart/nodetype/) { get; } | DevolucionesFieldStart . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Obtiene el padre inmediato de este nodo. |
| [ParentParagraph](../../aspose.words/inline/parentparagraph/) { get; } | Recupera el padre[`Paragraph`](../../aspose.words/paragraph/) de este nodo. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Obtiene el nodo inmediatamente anterior a este nodo. |
| [Range](../../aspose.words/node/range/) { get; } | Devuelve un **Rango** objeto que representa la parte de un documento que está contenido en este nodo. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| override [Accept](../../aspose.words.fields/fieldstart/accept/)(DocumentVisitor) | Acepta un visitante. |
| [Clone](../../aspose.words/node/clone/)(bool) | Crea un duplicado del nodo. |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | Obtiene el primer ancestro del especificado[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | Obtiene el primer ancestro del tipo de objeto especificado. |
| [GetField](../../aspose.words.fields/fieldchar/getfield/)() | Devuelve un campo para el campo char. |
| override [GetText](../../aspose.words/specialchar/gettext/)() | Obtiene el carácter especial que representa este nodo. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | Obtiene el siguiente nodo de acuerdo con el algoritmo de recorrido del árbol de pedido previo. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(Node) | Obtiene el nodo anterior de acuerdo con el algoritmo de recorrido del árbol de pedido previo. |
| [Remove](../../aspose.words/node/remove/)() | Se elimina a sí mismo del padre. |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | Exporta el contenido del nodo a una cadena en el formato especificado. |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | Exporta el contenido del nodo a una cadena utilizando las opciones de guardado especificadas. |

### Observaciones

`FieldStart` es un nodo de nivel en línea y está representado por the [`FieldStartChar`](../../aspose.words/controlchar/fieldstartchar/) carácter de control en el documento.

`FieldStart` solo puede ser hijo de[`Paragraph`](../../aspose.words/paragraph/).

Un campo completo en un documento de Microsoft Word es una estructura compleja que consta de un carácter de inicio de campo, un código de campo, un carácter separador de campo, un resultado de campo y un carácter de fin de campo. Algunos campos solo tienen inicio de campo, código de campo y fin de campo.

Para insertar fácilmente un nuevo campo en un documento, use el[`InsertField`](../../aspose.words/documentbuilder/insertfield/) método .

### Ejemplos

Muestra cómo trabajar con una colección de campos.

```csharp
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.InsertField(" DATE \\@ \"dddd, d MMMM yyyy\" ");
    builder.InsertField(" TIME ");
    builder.InsertField(" REVNUM ");
    builder.InsertField(" AUTHOR  \"John Doe\" ");
    builder.InsertField(" SUBJECT \"My Subject\" ");
    builder.InsertField(" QUOTE \"Hello world!\" ");
    doc.UpdateFields();

    FieldCollection fields = doc.Range.Fields;

    Assert.AreEqual(6, fields.Count);

    // Iterar sobre la colección de campos e imprimir contenido y escribir
    // de cada campo usando una implementación de visitante personalizada.
    FieldVisitor fieldVisitor = new FieldVisitor();

    using (IEnumerator<Field> fieldEnumerator = fields.GetEnumerator())
    {
        while (fieldEnumerator.MoveNext())
        {
            if (fieldEnumerator.Current != null)
            {
                fieldEnumerator.Current.Start.Accept(fieldVisitor);
                fieldEnumerator.Current.Separator?.Accept(fieldVisitor);
                fieldEnumerator.Current.End.Accept(fieldVisitor);
            }
            else
            {
                Console.WriteLine("There are no fields in the document.");
            }
        }
    }

    Console.WriteLine(fieldVisitor.GetText());

/// <summary>
/// Implementación del visitante del documento que imprime la información del campo.
/// </summary>
public class FieldVisitor : DocumentVisitor
{
    public FieldVisitor()
    {
        mBuilder = new StringBuilder();
    }

    /// <summary>
    /// Obtiene el texto sin formato del documento que fue acumulado por el visitante.
    /// </summary>
    public string GetText()
    {
        return mBuilder.ToString();
    }

    /// <summary>
    /// Llamado cuando se encuentra un nodo FieldStart en el documento.
    /// </summary>
    public override VisitorAction VisitFieldStart(FieldStart fieldStart)
    {
        mBuilder.AppendLine("Found field: " + fieldStart.FieldType);
        mBuilder.AppendLine("\tField code: " + fieldStart.GetField().GetFieldCode());
        mBuilder.AppendLine("\tDisplayed as: " + fieldStart.GetField().Result);

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Llamado cuando se encuentra un nodo FieldSeparator en el documento.
    /// </summary>
    public override VisitorAction VisitFieldSeparator(FieldSeparator fieldSeparator)
    {
        mBuilder.AppendLine("\tFound separator: " + fieldSeparator.GetText());

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Llamado cuando se encuentra un nodo FieldEnd en el documento.
    /// </summary>
    public override VisitorAction VisitFieldEnd(FieldEnd fieldEnd)
    {
        mBuilder.AppendLine("End of field: " + fieldEnd.FieldType);

        return VisitorAction.Continue;
    }

    private readonly StringBuilder mBuilder;
}
```

Muestra cómo encontrar todos los hipervínculos en un documento de Word y luego cambiar sus direcciones URL y nombres para mostrar.

```csharp
using System;
using System.Linq;
using System.Text;
using System.Text.RegularExpressions;
using Aspose.Words;
using Aspose.Words.Fields;
using NUnit.Framework;

namespace ApiExamples
{
    public class ExReplaceHyperlinks : ApiExampleBase
    {
        public void Fields()
        {
            Document doc = new Document(MyDir + "Hyperlinks.docx");

            // Los hipervínculos en un documento de Word son campos. Para comenzar a buscar hipervínculos, primero debemos encontrar todos los campos.
            // Use el método "SelectNodes" para encontrar todos los campos en el documento a través de un XPath.
            NodeList fieldStarts = doc.SelectNodes("//InicioCampo");

            foreach (FieldStart fieldStart in fieldStarts.OfType<FieldStart>())
            {
                if (fieldStart.FieldType == FieldType.FieldHyperlink)
                {
                    Hyperlink hyperlink = new Hyperlink(fieldStart);

                    // Los hipervínculos que enlazan con marcadores no tienen URL.
                    if (hyperlink.IsLocal)
                        continue;

                    // Asigne a cada hipervínculo de URL una nueva URL y un nombre.
                    hyperlink.Target = NewUrl;
                    hyperlink.Name = NewName;
                }
            }

            doc.Save(ArtifactsDir + "ReplaceHyperlinks.Fields.docx");
        }

        private const string NewUrl = @"http://www.aspose.com";
        private const string NewName = "Aspose - The .NET & Java Component Publisher";
    }

    /// <summary>
    /// Los campos HYPERLINK contienen y muestran hipervínculos en el cuerpo del documento. Un campo en Aspose.Words 
    /// consta de varios nodos, y puede ser difícil trabajar con todos esos nodos directamente. 
    /// Esta implementación funcionará solo si el código y el nombre del hipervínculo constan cada uno de un solo nodo Ejecutar.
    ///
    /// La estructura de nodos para los campos es la siguiente:
    /// 
    /// [FieldStart][Ejecutar - código de campo][FieldSeparator][Ejecutar - resultado del campo][FieldEnd]
    /// 
    /// A continuación se muestran dos códigos de campo de ejemplo de campos de HIPERVÍNCULO:
    /// HIPERVÍNCULO "url"
    /// HIPERVÍNCULO \l "nombre del marcador"
    /// 
    /// La propiedad "Resultado" de un campo contiene texto que el campo muestra en el cuerpo del documento al usuario.
    /// </summary>
    internal class Hyperlink
    {
        internal Hyperlink(FieldStart fieldStart)
        {
            if (fieldStart == null)
                throw new ArgumentNullException("fieldStart");
            if (fieldStart.FieldType != FieldType.FieldHyperlink)
                throw new ArgumentException("Field start type must be FieldHyperlink.");

            mFieldStart = fieldStart;

            // Encuentra el nodo separador de campos.
            mFieldSeparator = FindNextSibling(mFieldStart, NodeType.FieldSeparator);
            if (mFieldSeparator == null)
                throw new InvalidOperationException("Cannot find field separator.");

            // Normalmente, siempre podemos encontrar el nodo final del campo, pero el documento de ejemplo 
            // contiene un salto de párrafo dentro de un hipervínculo, que pone el final del campo 
            // en el siguiente párrafo. Será mucho más complicado manejar campos que abarquen varios 
            // párrafos correctamente. En este caso, permitir que el fin del campo sea nulo es suficiente.
            mFieldEnd = FindNextSibling(mFieldSeparator, NodeType.FieldEnd);

            // El código de campo se parece a "HIPERVINCULO "http:\\www.myurl.com"", pero puede constar de varias ejecuciones.
            string fieldCode = GetTextSameParent(mFieldStart.NextSibling, mFieldSeparator);
            Match match = gRegex.Match(fieldCode.Trim());

            // El hipervínculo es local si \l está presente en el código de campo.
            mIsLocal = match.Groups[1].Length > 0; 
            mTarget = match.Groups[2].Value;
        }

        /// <summary>
        /// Obtiene o establece el nombre para mostrar del hipervínculo.
        /// </summary>
        internal string Name
        {
            get => GetTextSameParent(mFieldSeparator, mFieldEnd); 
            set
            {
                // El nombre para mostrar del hipervínculo se almacena en el resultado del campo, que es Ejecutar 
                // nodo entre el separador de campo y el final del campo.
                Run fieldResult = (Run) mFieldSeparator.NextSibling;
                fieldResult.Text = value;

                // Si el resultado del campo consta de más de una ejecución, elimine estas ejecuciones.
                RemoveSameParent(fieldResult.NextSibling, mFieldEnd);
            }
        }

        /// <summary>
        /// Obtiene o establece la URL de destino o el nombre del marcador del hipervínculo.
        /// </summary>
        internal string Target
        {
            get => mTarget;
            set
            {
                mTarget = value;
                UpdateFieldCode();
            }
        }

        /// <summary>
        /// Verdadero si el objetivo de los hipervínculos es un marcador dentro del documento. Falso si el hipervínculo es una URL.
        /// </summary>
        internal bool IsLocal
        {
            get => mIsLocal; 
            set
            {
                mIsLocal = value;
                UpdateFieldCode();
            }
        }

        private void UpdateFieldCode()
        {
            // El código de campo de un campo está en un nodo Ejecutar entre el nodo de inicio del campo y el separador de campo.
            Run fieldCode = (Run) mFieldStart.NextSibling;
            fieldCode.Text = string.Format("HYPERLINK {0}\"{1}\"", ((mIsLocal) ? "\\l " : ""), mTarget);

            // Si el código de campo consta de más de una ejecución, elimine estas ejecuciones.
            RemoveSameParent(fieldCode.NextSibling, mFieldSeparator);
        }

        /// <summary>
        /// Pasa por los hermanos a partir del nodo de inicio hasta que encuentra un nodo del tipo especificado o nulo.
        /// </summary>
        private static Node FindNextSibling(Node startNode, NodeType nodeType)
        {
            for (Node node = startNode; node != null; node = node.NextSibling)
            {
                if (node.NodeType == nodeType)
                    return node;
            }

            return null;
        }

        /// <summary>
        /// Recupera texto desde el inicio hasta el nodo final, pero sin incluirlo.
        /// </summary>
        private static string GetTextSameParent(Node startNode, Node endNode)
        {
            if ((endNode != null) && (startNode.ParentNode != endNode.ParentNode))
                throw new ArgumentException("Start and end nodes are expected to have the same parent.");

            StringBuilder builder = new StringBuilder();
            for (Node child = startNode; !child.Equals(endNode); child = child.NextSibling)
                builder.Append(child.GetText());

            return builder.ToString();
        }

        /// <summary>
        /// Elimina nodos desde el inicio hasta el nodo final, pero sin incluirlo.
        /// Supone que los nodos inicial y final tienen el mismo padre.
        /// </summary>
        private static void RemoveSameParent(Node startNode, Node endNode)
        {
            if (endNode != null && startNode.ParentNode != endNode.ParentNode)
                throw new ArgumentException("Start and end nodes are expected to have the same parent.");

            Node curChild = startNode;
            while ((curChild != null) && (curChild != endNode))
            {
                Node nextChild = curChild.NextSibling;
                curChild.Remove();
                curChild = nextChild;
            }
        }

        private readonly Node mFieldStart;
        private readonly Node mFieldSeparator;
        private readonly Node mFieldEnd;
        private bool mIsLocal;
        private string mTarget;

        private static readonly Regex gRegex = new Regex(
            "\\S+" + // Uno o más HIPERVÍNCULOS sin espacios u otra palabra en otros idiomas.
            "\\s+" + // Uno o más espacios.
            "(?:\"\"\\s+)?" + // No captura opcional "" y uno o más espacios.
            "(\\\\l\\s+)?" + // Indicador \l opcional seguido de uno o más espacios.
            "\"" + // Un apóstrofe.    
            "([^\"]+)" + // Uno o más caracteres, excluyendo el apóstrofo (objetivo del hipervínculo).
            "\"" // Un apóstrofe de cierre.
        );
    }
}
```

### Ver también

* class [FieldChar](../fieldchar/)
* espacio de nombres [Aspose.Words.Fields](../../aspose.words.fields/)
* asamblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
