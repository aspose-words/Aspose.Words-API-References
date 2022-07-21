---
title: NodeList
second_title: Référence de l'API Aspose.Words pour .NET
description: Représente une collection de nœuds correspondant à une requête XPath exécutée à laide deSelectNodes./compositenode/selectnodes méthode.
type: docs
weight: 3980
url: /fr/net/aspose.words/nodelist/
---
## NodeList class

Représente une collection de nœuds correspondant à une requête XPath exécutée à l'aide de[`SelectNodes`](../compositenode/selectnodes) méthode.

```csharp
public class NodeList : IEnumerable<Node>
```

## Propriétés

| Nom | La description |
| --- | --- |
| [Count](../../aspose.words/nodelist/count) { get; } | Obtient le nombre de nœuds dans la liste. |
| [Item](../../aspose.words/nodelist/item) { get; } | Récupère un nœud à l'index donné. |

## Méthodes

| Nom | La description |
| --- | --- |
| [GetEnumerator](../../aspose.words/nodelist/getenumerator)() | Fournit une simple itération de style "foreach" sur la collection de nœuds. |
| [ToArray](../../aspose.words/nodelist/toarray)() | Copie tous les nœuds de la collection vers un nouveau tableau de nœuds. |

### Remarques

**Liste de nœuds** est renvoyé par[`SelectNodes`](../compositenode/selectnodes) et contient une collection de nœuds correspondant à la requête XPath.

**Liste de nœuds** prend en charge l'accès indexé et l'itération.

Traiter le **Liste de nœuds** collection en tant que collection "instantanée". **Liste de nœuds**starts en tant que collection "live" car les nœuds ne sont pas réellement récupérés lorsque la requête XPath est exécutée. Les nœuds ne sont récupérés qu'à l'accès et à ce moment, le nœud et tous les nœuds qui le précèdent sont mis en cache pour former une collection "instantanée".

### Exemples

Montre comment rechercher tous les liens hypertexte dans un document Word, puis modifier leurs URL et noms d'affichage.

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

            // Les hyperliens dans un document Word sont des champs. Pour commencer à chercher des hyperliens, nous devons d'abord trouver tous les champs.
            // Utilisez la méthode "SelectNodes" pour retrouver tous les champs du document via un XPath.
            NodeList fieldStarts = doc.SelectNodes("//FieldStart");

            foreach (FieldStart fieldStart in fieldStarts.OfType<FieldStart>())
            {
                if (fieldStart.FieldType == FieldType.FieldHyperlink)
                {
                    Hyperlink hyperlink = new Hyperlink(fieldStart);

                    // Les hyperliens qui pointent vers des signets n'ont pas d'URL.
                    if (hyperlink.IsLocal)
                        continue;

                    // Donnez à chaque lien hypertexte URL une nouvelle URL et un nouveau nom.
                    hyperlink.Target = NewUrl;
                    hyperlink.Name = NewName;
                }
            }

            doc.Save(ArtifactsDir + "ReplaceHyperlinks.Fields.docx");
        }

        private const string NewUrl = @"http://www.aspose.com" ;
        private const string NewName = "Aspose - The .NET & Java Component Publisher";
    }

    /// <summary>
    /// Les champs HYPERLINK contiennent et affichent des hyperliens dans le corps du document. Un champ dans Aspose.Words 
    /// se compose de plusieurs nœuds, et il peut être difficile de travailler directement avec tous ces nœuds. 
    /// Cette implémentation ne fonctionnera que si le code et le nom du lien hypertexte consistent chacun en un seul nœud Run.
    ///
    /// La structure des nœuds pour les champs est la suivante :
    /// 
    /// [FieldStart][Exécuter - code de champ][FieldSeparator][Exécuter - résultat de champ][FieldEnd]
    /// 
    /// Vous trouverez ci-dessous deux exemples de codes de champs de champs HYPERLINK :
    /// HYPERLIEN "url"
    /// HYPERLINK \l "nom du signet"
    /// 
    /// La propriété "Result" d'un champ contient le texte que le champ affiche dans le corps du document à l'utilisateur.
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

            // Trouver le nœud séparateur de champ.
            mFieldSeparator = FindNextSibling(mFieldStart, NodeType.FieldSeparator);
            if (mFieldSeparator == null)
                throw new InvalidOperationException("Cannot find field separator.");

            // Normalement, nous pouvons toujours trouver le nœud de fin du champ, mais le document d'exemple 
            // contient un saut de paragraphe à l'intérieur d'un lien hypertexte, qui met fin au champ 
            // dans le paragraphe suivant. Il sera beaucoup plus compliqué de gérer des champs qui s'étendent sur plusieurs 
            // paragraphes correctement. Dans ce cas, autoriser la fin du champ à être nulle suffit.
            mFieldEnd = FindNextSibling(mFieldSeparator, NodeType.FieldEnd);

            // Le code de champ ressemble à "HYPERLINK "http:\\www.myurl.com"", mais il peut consister en plusieurs exécutions.
            string fieldCode = GetTextSameParent(mFieldStart.NextSibling, mFieldSeparator);
            Match match = gRegex.Match(fieldCode.Trim());

            // Le lien hypertexte est local si \l est présent dans le code du champ.
            mIsLocal = match.Groups[1].Length > 0; 
            mTarget = match.Groups[2].Value;
        }

        /// <summary>
        /// Obtient ou définit le nom d'affichage du lien hypertexte.
        /// </summary>
        internal string Name
        {
            get => GetTextSameParent(mFieldSeparator, mFieldEnd); 
            set
            {
                // Le nom d'affichage du lien hypertexte est stocké dans le résultat du champ, qui est une exécution 
                // nœud entre le séparateur de champ et la fin du champ.
                Run fieldResult = (Run) mFieldSeparator.NextSibling;
                fieldResult.Text = value;

                // Si le résultat du champ consiste en plusieurs exécutions, supprimez ces exécutions.
                RemoveSameParent(fieldResult.NextSibling, mFieldEnd);
            }
        }

        /// <summary>
        /// Récupère ou définit l'URL cible ou le nom du signet du lien hypertexte.
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
        /// Vrai si la cible des liens hypertexte est un signet à l'intérieur du document. Faux si le lien hypertexte est une URL.
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
            // Le code de champ d'un champ se trouve dans un nœud Run entre le nœud de début du champ et le séparateur de champs.
            Run fieldCode = (Run) mFieldStart.NextSibling;
            fieldCode.Text = string.Format("HYPERLINK {0}\"{1}\"", ((mIsLocal) ? "\\l " : ""), mTarget);

            // Si le code de champ se compose de plusieurs exécutions, supprimez ces exécutions.
            RemoveSameParent(fieldCode.NextSibling, mFieldSeparator);
        }

        /// <summary>
        /// Parcourt les frères et sœurs à partir du nœud de départ jusqu'à ce qu'il trouve un nœud du type spécifié ou nul.
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
        /// Récupère le texte du début jusqu'au nœud de fin non compris.
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
        /// Supprime les nœuds du début jusqu'au nœud de fin, mais sans l'inclure.
        /// Suppose que les nœuds de début et de fin ont le même parent.
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
            "\\S+" + // Un ou plusieurs HYPERLINK non espaces ou un autre mot dans d'autres langues.
            "\\s+" + // Un ou plusieurs espaces.
            "(?:\"\"\\s+)?" + // "" facultatif non capturant et un ou plusieurs espaces.
            "(\\\\l\\s+)?" + // Indicateur \l facultatif suivi d'un ou plusieurs espaces.
            "\"" + // Une apostrophe.    
            "([^\"]+)" + // Un ou plusieurs caractères, à l'exclusion de l'apostrophe (cible du lien hypertexte).
            "\"" // Une apostrophe fermante.
        );
    }
}
```

### Voir également

* class [Node](../node)
* espace de noms [Aspose.Words](../../aspose.words)
* Assemblée [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
