---
title: NodeList Class
linktitle: NodeList
articleTitle: NodeList
second_title: Aspose.Words para .NET
description: Explore la clase Aspose.Words.NodeList, su solución ideal para administrar de manera eficiente los resultados de consultas XPath y mejorar las capacidades de procesamiento de documentos.
type: docs
weight: 4910
url: /es/net/aspose.words/nodelist/
---
## NodeList class

Representa una colección de nodos que coinciden con una consulta XPath ejecutada utilizando el[`SelectNodes`](../compositenode/selectnodes/) método.

Para obtener más información, visite el[Modelo de objetos de documento (DOM) de Aspose.Words](https://docs.aspose.com/words/net/aspose-words-document-object-model/) Artículo de documentación.

```csharp
public class NodeList : IEnumerable<Node>
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Count](../../aspose.words/nodelist/count/) { get; } | Obtiene el número de nodos en la lista. |
| [Item](../../aspose.words/nodelist/item/) { get; } | Recupera un nodo en el índice dado. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [GetEnumerator](../../aspose.words/nodelist/getenumerator/)() | Proporciona una iteración simple al estilo "foreach" sobre la colección de nodos. |
| [ToArray](../../aspose.words/nodelist/toarray/)() | Copia todos los nodos de la colección a una nueva matriz de nodos. |

## Observaciones

`NodeList` es devuelto por[`SelectNodes`](../compositenode/selectnodes/) y contiene una colección de nodos que coinciden con la consulta XPath.

`NodeList` Admite acceso indexado e iteración.

Tratar el`NodeList` colección como una colección "instantánea".`NodeList` starts como una colección "en vivo" porque los nodos no se recuperan realmente cuando se ejecuta la consulta XPath. Los nodos solo se recuperan al acceder y en este momento el nodo y todos los nodos que lo preceden se almacenan en caché formando una colección de "instantánea".

## Ejemplos

Muestra cómo encontrar todos los hipervínculos en un documento de Word y luego cambiar sus URL y nombres para mostrar.

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

            Los hipervínculos en un documento de Word son campos. Para buscar hipervínculos, primero debemos encontrar todos los campos.
            // Utilice el método "SelectNodes" para encontrar todos los campos del documento a través de un XPath.
            NodeList fieldStarts = doc.SelectNodes("//CampoInicio");

            foreach (FieldStart fieldStart in fieldStarts.OfType<FieldStart>())
            {
                if (fieldStart.FieldType == FieldType.FieldHyperlink)
                {
                    Hyperlink hyperlink = new Hyperlink(fieldStart);

                    // Los hipervínculos que enlazan a marcadores no tienen URL.
                    if (hyperlink.IsLocal)
                        continue;

                    // Dale a cada hipervínculo URL una nueva URL y un nombre.
                    hyperlink.Target = NewUrl;
                    hyperlink.Name = NewName;
                }
            }

            doc.Save(ArtifactsDir + "ReplaceHyperlinks.Fields.docx");
        }

        private const string NewUrl = @"http://www.aspose.com";
        private const string NewName = "Aspose - The .NET & Java Component Publisher";
    }

     ///<summary>
      ///Los campos HIPERVÍNCULO contienen y muestran hipervínculos en el cuerpo del documento. Un campo en Aspose.Words
      ///consta de varios nodos y podría resultar difícil trabajar con todos esos nodos directamente.
     ///Esta implementación funcionará solo si el código y el nombre del hipervínculo constan cada uno de un solo nodo Ejecutar.
    ///
     ///La estructura del nodo para los campos es la siguiente:
     ///
     ///[FieldStart][Run - field code][FieldSeparator][Run - field result][FieldEnd]
     ///
     ///Below are two example field codes of HYPERLINK fields:
     ///HYPERLINK "url"
     ///HYPERLINK \l "bookmark name"
     ///
     ///A field's "Result" property contains text that the field displays in the document body to the user.
     ///</summary>
    internal class Hyperlink
    {
        internal Hyperlink(FieldStart fieldStart)
        {
            if (fieldStart == null)
                throw new ArgumentNullException("fieldStart");
            if (fieldStart.FieldType != FieldType.FieldHyperlink)
                throw new ArgumentException("Field start type must be FieldHyperlink.");

            mFieldStart = fieldStart;

            // Encuentra el nodo separador de campo.
            mFieldSeparator = FindNextSibling(mFieldStart, NodeType.FieldSeparator);
            if (mFieldSeparator == null)
                throw new InvalidOperationException("Cannot find field separator.");

             // Normalmente, siempre podemos encontrar el nodo final del campo, pero el documento de ejemplo
             // contiene un salto de párrafo dentro de un hipervínculo, que coloca el campo al final
             // en el siguiente párrafo. Será mucho más complicado manejar campos que abarcan varios
            // Los párrafos se escriben correctamente. En este caso, basta con que el campo final sea nulo.
            mFieldEnd = FindNextSibling(mFieldSeparator, NodeType.FieldEnd);

            // El código de campo se parece a algo como "HIPERVÍNCULO "http:\\www.myurl.com"", pero puede constar de varias ejecuciones.
            string fieldCode = GetTextSameParent(mFieldStart.NextSibling, mFieldSeparator);
            Match match = gRegex.Match(fieldCode.Trim());

            // El hipervínculo es local si \l está presente en el código de campo.
            mIsLocal = match.Groups[1].Length > 0; 
            mTarget = match.Groups[2].Value;
        }

         ///<summary>
         ///Gets or sets the display name of the hyperlink.
         ///</summary>
        internal string Name
        {
            get
            {
                return GetTextSameParent(mFieldSeparator, mFieldEnd);
            }
            set
            {
                 // El nombre para mostrar del hipervínculo se almacena en el resultado del campo, que es una ejecución
                // nodo entre el separador de campo y el final del campo.
                Run fieldResult = (Run) mFieldSeparator.NextSibling;
                fieldResult.Text = value;

                // Si el resultado del campo consta de más de una ejecución, elimine estas ejecuciones.
                RemoveSameParent(fieldResult.NextSibling, mFieldEnd);
            }
        }

         ///<summary>
         ///Gets or sets the target URL or bookmark name of the hyperlink.
         ///</summary>
        internal string Target
        {
            get
            {
                return mTarget;
            }
            set
            {
                mTarget = value;
                UpdateFieldCode();
            }
        }

         ///<summary>
         ///True if the hyperlinks target is a bookmark inside the document. False if the hyperlink is a URL.
         ///</summary>
        internal bool IsLocal
        {
            get
            {
                return mIsLocal;
            }
            set
            {
                mIsLocal = value;
                UpdateFieldCode();
            }
        }

        private void UpdateFieldCode()
        {
            // El código de campo de un campo está en un nodo de ejecución entre el nodo de inicio del campo y el separador de campo.
            Run fieldCode = (Run) mFieldStart.NextSibling;
            fieldCode.Text = string.Format("HYPERLINK {0}\"{1}\"", ((mIsLocal) ? "\\l " : ""), mTarget);

            // Si el código de campo consta de más de una ejecución, elimine estas ejecuciones.
            RemoveSameParent(fieldCode.NextSibling, mFieldSeparator);
        }

         ///<summary>
         ///Goes through siblings starting from the start node until it finds a node of the specified type or null.
         ///</summary>
        private static Node FindNextSibling(Node startNode, NodeType nodeType)
        {
            for (Node node = startNode; node != null; node = node.NextSibling)
            {
                if (node.NodeType == nodeType)
                    return node;
            }

            return null;
        }

         ///<summary>
         ///Retrieves text from start up to but not including the end node.
         ///</summary>
        private static string GetTextSameParent(Node startNode, Node endNode)
        {
            if ((endNode != null) && (startNode.ParentNode != endNode.ParentNode))
                throw new ArgumentException("Start and end nodes are expected to have the same parent.");

            StringBuilder builder = new StringBuilder();
            for (Node child = startNode; !child.Equals(endNode); child = child.NextSibling)
                builder.Append(child.GetText());

            return builder.ToString();
        }

         ///<summary>
         ///Removes nodes from start up to but not including the end node.
         ///Assumes that the start and end nodes have the same parent.
         ///</summary>
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
            "\\S+" + // Uno o más HIPERVÍNCULO que no sean espacios u otra palabra en otros idiomas.
            "\\s+" + //Uno o más espacios.
            "(?:\"\"\\s+)?" + // No se captura "" opcional y uno o más espacios.
            "(\\\\l\\s+)?" + // Bandera opcional \l seguida de uno o más espacios.
            "\"" +  // Un apóstrofe.
            "([^\"]+)" + // Uno o más caracteres, excluyendo el apóstrofe (objetivo del hipervínculo).
            "\"" // Un apóstrofe de cierre.
        );
    }
}
```

### Ver también

* class [Node](../node/)
* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)
