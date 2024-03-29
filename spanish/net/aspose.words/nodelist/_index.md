---
title: NodeList Class
linktitle: NodeList
articleTitle: NodeList
second_title: Aspose.Words para .NET
description: Aspose.Words.NodeList clase. Representa una colección de nodos que coinciden con una consulta XPath ejecutada utilizando elSelectNodes método en C#.
type: docs
weight: 4220
url: /es/net/aspose.words/nodelist/
---
## NodeList class

Representa una colección de nodos que coinciden con una consulta XPath ejecutada utilizando el[`SelectNodes`](../compositenode/selectnodes/) método.

Para obtener más información, visite el[Modelo de objetos de documento (DOM) de Aspose.Words](https://docs.aspose.com/words/net/aspose-words-document-object-model/) artículo de documentación.

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
| [GetEnumerator](../../aspose.words/nodelist/getenumerator/)() | Proporciona una iteración de estilo "foreach" simple sobre la colección de nodos. |
| [ToArray](../../aspose.words/nodelist/toarray/)() | Copia todos los nodos de la colección en una nueva matriz de nodos. |

## Observaciones

`NodeList` es devuelto por[`SelectNodes`](../compositenode/selectnodes/) y contiene una colección de nodos que coinciden con la consulta XPath.

`NodeList` admite acceso indexado e iteración.

Tratar el`NodeList` colección como una colección "instantánea".`NodeList`comienza como una colección "activa" porque los nodos en realidad no se recuperan cuando se ejecuta la consulta XPath. Los nodos sólo se recuperan al acceder y en este momento el nodo y todos los nodos que lo preceden se almacenan en caché formando una colección "instantánea".

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

            // Los hipervínculos en documentos de Word son campos. Para comenzar a buscar hipervínculos, primero debemos encontrar todos los campos.
            // Utilice el método "SelectNodes" para buscar todos los campos del documento mediante un XPath.
            NodeList fieldStarts = doc.SelectNodes("//Inicio de campo");

            foreach (FieldStart fieldStart in fieldStarts.OfType<FieldStart>())
            {
                if (fieldStart.FieldType == FieldType.FieldHyperlink)
                {
                    Hyperlink hyperlink = new Hyperlink(fieldStart);

                    // Los hipervínculos que enlazan con marcadores no tienen URL.
                    if (hyperlink.IsLocal)
                        continue;

                    // Asigne a cada hipervínculo URL una nueva URL y nombre.
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
      ///consta de varios nodos y puede resultar difícil trabajar con todos esos nodos directamente.
     ///Esta implementación funcionará solo si el código del hipervínculo y el nombre constan cada uno de un solo nodo Ejecutar.
    ///
     ///La estructura de nodos para los campos es la siguiente:
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

            // Encuentra el nodo separador de campos.
            mFieldSeparator = FindNextSibling(mFieldStart, NodeType.FieldSeparator);
            if (mFieldSeparator == null)
                throw new InvalidOperationException("Cannot find field separator.");

             // Normalmente, siempre podemos encontrar el nodo final del campo, pero el documento de ejemplo
             // contiene un salto de párrafo dentro de un hipervínculo, que coloca el campo al final
            // en el siguiente párrafo. Será mucho más complicado manejar campos que abarquen varios
            // párrafos correctamente. En este caso, basta con permitir que el final del campo sea nulo.
            mFieldEnd = FindNextSibling(mFieldSeparator, NodeType.FieldEnd);

            // El código de campo se parece a "HIPERVÍNCULO "http:\\www.myurl.com"", pero puede constar de varias ejecuciones.
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
            get => GetTextSameParent(mFieldSeparator, mFieldEnd); 
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
            get => mTarget;
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
            "\\S+" + // Uno o más HIPERVÍNCULOS sin espacios u otra palabra en otros idiomas.
            "\\s+" + // Uno o más espacios.
            "(?:\"\"\\s+)?" + // Opcional "" sin captura y uno o más espacios.
            "(\\\\l\\s+)?" + // Indicador \l opcional seguido de uno o más espacios.
            "\"" +  // Un apóstrofe.
            "([^\"]+)" + // Uno o más caracteres, excluyendo el apóstrofe (destino del hipervínculo).
            "\"" // Un apóstrofe de cierre.
        );
    }
}
```

### Ver también

* class [Node](../node/)
* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)
