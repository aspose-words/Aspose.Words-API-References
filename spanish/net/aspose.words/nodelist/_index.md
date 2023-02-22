---
title: Class NodeList
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.NodeList clase. Representa una colección de nodos que coinciden con una consulta XPath ejecutada mediante elSelectNodes método.
type: docs
weight: 3980
url: /es/net/aspose.words/nodelist/
---
## NodeList class

Representa una colección de nodos que coinciden con una consulta XPath ejecutada mediante el[`SelectNodes`](../compositenode/selectnodes/) método.

```csharp
public class NodeList : IEnumerable<Node>
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Count](../../aspose.words/nodelist/count/) { get; } | Obtiene el número de nodos de la lista. |
| [Item](../../aspose.words/nodelist/item/) { get; } | Recupera un nodo en el índice dado. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [GetEnumerator](../../aspose.words/nodelist/getenumerator/)() | Proporciona una iteración de estilo "foreach" simple sobre la colección de nodos. |
| [ToArray](../../aspose.words/nodelist/toarray/)() | Copia todos los nodos de la colección a una nueva matriz de nodos. |

### Observaciones

**lista de nodos** es devuelto por[`SelectNodes`](../compositenode/selectnodes/) y contiene una colección de nodos que coinciden con la consulta XPath.

**lista de nodos** admite el acceso indexado y la iteración.

tratar el **lista de nodos** colección como una colección "instantánea". **lista de nodos**comienza como una colección "viva" porque los nodos no se recuperan realmente cuando se ejecuta la consulta XPath. Los nodos solo se recuperan al acceder y, en este momento, el nodo y todos los nodos que lo preceden se almacenan en caché para formar una colección "instantánea".

### Ejemplos

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

* class [Node](../node/)
* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)


