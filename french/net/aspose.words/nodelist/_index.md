---
title: NodeList Class
linktitle: NodeList
articleTitle: NodeList
second_title: Aspose.Words pour .NET
description: Explorez la classe Aspose.Words.NodeList, votre solution de référence pour gérer efficacement les résultats des requêtes XPath et améliorer les capacités de traitement des documents.
type: docs
weight: 4910
url: /fr/net/aspose.words/nodelist/
---
## NodeList class

Représente une collection de nœuds correspondant à une requête XPath exécutée à l'aide de[`SelectNodes`](../compositenode/selectnodes/) méthode.

Pour en savoir plus, visitez le[Modèle d'objet de document (DOM) Aspose.Words](https://docs.aspose.com/words/net/aspose-words-document-object-model/) article de documentation.

```csharp
public class NodeList : IEnumerable<Node>
```

## Propriétés

| Nom | La description |
| --- | --- |
| [Count](../../aspose.words/nodelist/count/) { get; } | Obtient le nombre de nœuds dans la liste. |
| [Item](../../aspose.words/nodelist/item/) { get; } | Récupère un nœud à l'index donné. |

## Méthodes

| Nom | La description |
| --- | --- |
| [GetEnumerator](../../aspose.words/nodelist/getenumerator/)() | Fournit une itération simple de style « foreach » sur la collection de nœuds. |
| [ToArray](../../aspose.words/nodelist/toarray/)() | Copie tous les nœuds de la collection vers un nouveau tableau de nœuds. |

## Remarques

`NodeList` est renvoyé par[`SelectNodes`](../compositenode/selectnodes/) et contient une collection de nœuds correspondant à la requête XPath.

`NodeList` prend en charge l'accès indexé et l'itération.

Traiter le`NodeList` collection comme une collection « instantané ».`NodeList` starts comme une collection « live » car les nœuds ne sont pas réellement récupérés lorsque la requête XPath est exécutée. Les nœuds ne sont récupérés que lors de l'accès et à ce moment-là, le nœud et tous les nœuds qui le précèdent sont mis en cache formant une collection « snapshot ».

## Exemples

Montre comment rechercher tous les hyperliens dans un document Word, puis modifier leurs URL et leurs noms d’affichage.

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

            // Les hyperliens dans un document Word sont des champs. Pour rechercher des hyperliens, il faut d'abord trouver tous les champs.
            // Utilisez la méthode « SelectNodes » pour rechercher tous les champs du document via un XPath.
            NodeList fieldStarts = doc.SelectNodes("//Début du champ");

            foreach (FieldStart fieldStart in fieldStarts.OfType<FieldStart>())
            {
                if (fieldStart.FieldType == FieldType.FieldHyperlink)
                {
                    Hyperlink hyperlink = new Hyperlink(fieldStart);

                    // Les hyperliens qui renvoient vers des signets n'ont pas d'URL.
                    if (hyperlink.IsLocal)
                        continue;

                    // Donnez à chaque lien hypertexte URL une nouvelle URL et un nouveau nom.
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
      ///Les champs HYPERLINK contiennent et affichent des hyperliens dans le corps du document. Un champ dans Aspose.Words
      ///se compose de plusieurs nœuds, et il peut être difficile de travailler directement avec tous ces nœuds.
     ///Cette implémentation ne fonctionnera que si le code et le nom du lien hypertexte se composent chacun d'un seul nœud Exécuter.
    ///
     ///La structure des nœuds pour les champs est la suivante :
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

            // Rechercher le nœud séparateur de champ.
            mFieldSeparator = FindNextSibling(mFieldStart, NodeType.FieldSeparator);
            if (mFieldSeparator == null)
                throw new InvalidOperationException("Cannot find field separator.");

             // Normalement, nous pouvons toujours trouver le nœud de fin du champ, mais le document d'exemple
             // contient un saut de paragraphe à l'intérieur d'un lien hypertexte, ce qui met le champ à la fin
             // dans le paragraphe suivant. Il sera beaucoup plus compliqué de gérer des champs qui s'étendent sur plusieurs
            // Paragraphes correctement. Dans ce cas, autoriser la valeur null pour le champ end suffit.
            mFieldEnd = FindNextSibling(mFieldSeparator, NodeType.FieldEnd);

            // Le code du champ ressemble à quelque chose comme "HYPERLINK "http:\\www.myurl.com"", mais il peut être composé de plusieurs exécutions.
            string fieldCode = GetTextSameParent(mFieldStart.NextSibling, mFieldSeparator);
            Match match = gRegex.Match(fieldCode.Trim());

            // L'hyperlien est local si \l est présent dans le code du champ.
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
                 // Le nom d'affichage du lien hypertexte est stocké dans le champ résultat, qui est une exécution
                // nœud entre le séparateur de champ et la fin du champ.
                Run fieldResult = (Run) mFieldSeparator.NextSibling;
                fieldResult.Text = value;

                // Si le résultat du champ se compose de plusieurs exécutions, supprimez ces exécutions.
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
            // Le code de champ d'un champ se trouve dans un nœud Exécuter entre le nœud de départ du champ et le séparateur de champ.
            Run fieldCode = (Run) mFieldStart.NextSibling;
            fieldCode.Text = string.Format("HYPERLINK {0}\"{1}\"", ((mIsLocal) ? "\\l " : ""), mTarget);

            // Si le code de champ se compose de plusieurs exécutions, supprimez ces exécutions.
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
            "\\S+" + // Un ou plusieurs HYPERLINK ou autre mot non-espace dans d'autres langues.
            "\\s+" + // Un ou plusieurs espaces.
            "(?:\"\"\\s+)?" + // Facultatif non capturant "" et un ou plusieurs espaces.
            "(\\\\l\\s+)?" + // Indicateur facultatif \l suivi d'un ou plusieurs espaces.
            "\"" +  // Une apostrophe.
            "([^\"]+)" + // Un ou plusieurs caractères, à l'exclusion de l'apostrophe (cible du lien hypertexte).
            "\"" // Une apostrophe fermante.
        );
    }
}
```

### Voir également

* class [Node](../node/)
* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)
