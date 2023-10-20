---
title: NodeList Class
linktitle: NodeList
articleTitle: NodeList
second_title: Aspose.Words pour .NET
description: Aspose.Words.NodeList classe. Représente une collection de nœuds correspondant à une requête XPath exécutée à laide duSelectNodes méthode en C#.
type: docs
weight: 4220
url: /fr/net/aspose.words/nodelist/
---
## NodeList class

Représente une collection de nœuds correspondant à une requête XPath exécutée à l'aide du[`SelectNodes`](../compositenode/selectnodes/) méthode.

Pour en savoir plus, visitez le[Modèle objet de document (DOM) Aspose.Words](https://docs.aspose.com/words/net/aspose-words-document-object-model/) article documentaire.

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
| [GetEnumerator](../../aspose.words/nodelist/getenumerator/)() | Fournit une simple itération de style "foreach" sur la collection de nœuds. |
| [ToArray](../../aspose.words/nodelist/toarray/)() | Copie tous les nœuds de la collection vers un nouveau tableau de nœuds. |

## Remarques

`NodeList` est renvoyé par[`SelectNodes`](../compositenode/selectnodes/) et contient une collection de nœuds correspondant à la requête XPath.

`NodeList` prend en charge l’accès et l’itération indexés.

Traitez le`NodeList` collection sous forme de collection « instantané ».`NodeList`start en tant que collection "live" car les nœuds ne sont pas réellement récupérés lorsque la requête XPath est exécutée. Les nœuds ne sont récupérés qu'à l'accès et à ce moment, le nœud et tous les nœuds qui le précèdent sont mis en cache pour former une collection "instantané".

## Exemples

Montre comment rechercher tous les liens hypertexte dans un document Word, puis modifier leurs URL et leurs noms d’affichage.

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

            // Les hyperliens dans un document Word sont des champs. Pour commencer à chercher des hyperliens, il faut d’abord trouver tous les champs.
            // Utilisez la méthode "SelectNodes" pour retrouver tous les champs du document via un XPath.
            NodeList fieldStarts = doc.SelectNodes("//Début du champ");

            foreach (FieldStart fieldStart in fieldStarts.OfType<FieldStart>())
            {
                if (fieldStart.FieldType == FieldType.FieldHyperlink)
                {
                    Hyperlink hyperlink = new Hyperlink(fieldStart);

                    // Les hyperliens renvoyant vers des signets n'ont pas d'URL.
                    if (hyperlink.IsLocal)
                        continue;

                    // Attribue à chaque lien hypertexte URL une nouvelle URL et un nouveau nom.
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
      ///se compose de plusieurs nœuds et il peut être difficile de travailler directement avec tous ces nœuds.
     ///Cette implémentation ne fonctionnera que si le code et le nom du lien hypertexte sont chacun constitués d'un seul nœud Run.
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

            // Recherche le nœud séparateur de champ.
            mFieldSeparator = FindNextSibling(mFieldStart, NodeType.FieldSeparator);
            if (mFieldSeparator == null)
                throw new InvalidOperationException("Cannot find field separator.");

             // Normalement, on peut toujours trouver le nœud de fin du champ, mais le document exemple
             // contient un saut de paragraphe à l'intérieur d'un lien hypertexte, qui met le champ à la fin
            // dans le paragraphe suivant. Il sera beaucoup plus compliqué de gérer des champs qui s'étendent sur plusieurs
            // paragraphes correctement. Dans ce cas, il suffit de permettre à la fin du champ d'être nulle.
            mFieldEnd = FindNextSibling(mFieldSeparator, NodeType.FieldEnd);

            // Le code du champ ressemble à "HYPERLINK "http:\\www.myurl.com"", mais il peut être composé de plusieurs exécutions.
            string fieldCode = GetTextSameParent(mFieldStart.NextSibling, mFieldSeparator);
            Match match = gRegex.Match(fieldCode.Trim());

            // Le lien hypertexte est local si \l est présent dans le code du champ.
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
                 // Le nom d'affichage du lien hypertexte est stocké dans le résultat du champ, qui est un Run
                // nœud entre le séparateur de champ et la fin du champ.
                Run fieldResult = (Run) mFieldSeparator.NextSibling;
                fieldResult.Text = value;

                // Si le résultat du champ comprend plusieurs exécutions, supprimez ces exécutions.
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
            // Le code de champ d'un champ se trouve dans un nœud Exécuter entre le nœud de début du champ et le séparateur de champ.
            Run fieldCode = (Run) mFieldStart.NextSibling;
            fieldCode.Text = string.Format("HYPERLINK {0}\"{1}\"", ((mIsLocal) ? "\\l " : ""), mTarget);

            // Si le code de champ comprend plusieurs exécutions, supprimez ces exécutions.
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
            "\\S+" + // Un ou plusieurs HYPERLIEN sans espaces ou autre mot dans d'autres langues.
            "\\s+" + // Un ou plusieurs espaces.
            "(?:\"\"\\s+)?" + // Non-capture "" facultatif et un ou plusieurs espaces.
            "(\\\\l\\s+)?" + // Indicateur \l facultatif suivi d'un ou plusieurs espaces.
            "\"" +  // Une apostrophe.
            "([^\"]+)" + // Un ou plusieurs caractères, hors apostrophe (cible du lien hypertexte).
            "\"" // Une apostrophe fermante.
        );
    }
}
```

### Voir également

* class [Node](../node/)
* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)
