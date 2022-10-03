---
title: FieldStart
second_title: Référence de l'API Aspose.Words pour .NET
description: Représente le début dun champ Word dans un document.
type: docs
weight: 2280
url: /fr/net/aspose.words.fields/fieldstart/
---
## FieldStart class

Représente le début d'un champ Word dans un document.

```csharp
public class FieldStart : FieldChar
```

## Propriétés

| Nom | La description |
| --- | --- |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Spécifie l'identifiant de nœud personnalisé. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Obtient le document auquel ce nœud appartient. |
| [FieldData](../../aspose.words.fields/fieldstart/fielddata/) { get; } | Obtient les données de champ personnalisées associées au champ. |
| [FieldType](../../aspose.words.fields/fieldchar/fieldtype/) { get; } | Renvoie le type du champ. |
| [Font](../../aspose.words/inline/font/) { get; } | Fournit l'accès à la mise en forme de la police de cet objet. |
| virtual [IsComposite](../../aspose.words/node/iscomposite/) { get; } | Renvoie true si ce nœud peut contenir d'autres nœuds. |
| [IsDeleteRevision](../../aspose.words/inline/isdeleterevision/) { get; } | Renvoie true si cet objet a été supprimé dans Microsoft Word alors que le suivi des modifications était activé. |
| [IsDirty](../../aspose.words.fields/fieldchar/isdirty/) { get; set; } | Obtient ou définit si le résultat actuel du champ n'est plus correct (périmé) en raison d'autres modifications apportées au document. |
| [IsFormatRevision](../../aspose.words/inline/isformatrevision/) { get; } | Renvoie true si la mise en forme de l'objet a été modifiée dans Microsoft Word alors que le suivi des modifications était activé. |
| [IsInsertRevision](../../aspose.words/inline/isinsertrevision/) { get; } | Renvoie true si cet objet a été inséré dans Microsoft Word alors que le suivi des modifications était activé. |
| [IsLocked](../../aspose.words.fields/fieldchar/islocked/) { get; set; } | Obtient ou définit si le champ parent est verrouillé (ne doit pas recalculer son résultat). |
| [IsMoveFromRevision](../../aspose.words/inline/ismovefromrevision/) { get; } | Retours **vrai** si cet objet a été déplacé (supprimé) dans Microsoft Word alors que le suivi des modifications était activé. |
| [IsMoveToRevision](../../aspose.words/inline/ismovetorevision/) { get; } | Retours **vrai** si cet objet a été déplacé (inséré) dans Microsoft Word alors que le suivi des modifications était activé. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Obtient le nœud suivant immédiatement ce nœud. |
| override [NodeType](../../aspose.words.fields/fieldstart/nodetype/) { get; } | RetoursFieldStart . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Obtient le parent immédiat de ce nœud. |
| [ParentParagraph](../../aspose.words/inline/parentparagraph/) { get; } | Récupère le parent[`Paragraph`](../../aspose.words/paragraph/) de ce nœud. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Obtient le nœud précédant immédiatement ce nœud. |
| [Range](../../aspose.words/node/range/) { get; } | Renvoie un **Intervalle** objet qui représente la partie d'un document contenue dans ce nœud. |

## Méthodes

| Nom | La description |
| --- | --- |
| override [Accept](../../aspose.words.fields/fieldstart/accept/)(DocumentVisitor) | Accepte un visiteur. |
| [Clone](../../aspose.words/node/clone/)(bool) | Crée un doublon du nœud. |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | Obtient le premier ancêtre du spécifié[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | Obtient le premier ancêtre du type d'objet spécifié. |
| [GetField](../../aspose.words.fields/fieldchar/getfield/)() | Renvoie un champ pour le champ car. |
| override [GetText](../../aspose.words/specialchar/gettext/)() | Obtient le caractère spécial que ce nœud représente. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | Obtient le nœud suivant selon l'algorithme de traversée de l'arbre de pré-ordre. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(Node) | Obtient le nœud précédent selon l'algorithme de parcours de l'arbre de pré-ordre. |
| [Remove](../../aspose.words/node/remove/)() | Se supprime du parent. |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | Exporte le contenu du nœud dans une chaîne au format spécifié. |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | Exporte le contenu du nœud dans une chaîne à l'aide des options d'enregistrement spécifiées. |

### Remarques

[`FieldStart`](./fieldstart/) est un nœud de niveau en ligne et représenté par the [`FieldStartChar`](../../aspose.words/controlchar/fieldstartchar/) caractère de contrôle dans le document.

[`FieldStart`](./fieldstart/) ne peut être qu'un enfant de[`Paragraph`](../../aspose.words/paragraph/).

Un champ complet dans un document Microsoft Word est une structure complexe composée de un caractère de début de champ, un code de champ, un caractère séparateur de champ, un résultat de champ et un caractère de fin de champ. Certains champs n'ont qu'un début de champ, un code de champ et une fin de champ.

Pour insérer facilement un nouveau champ dans un document, utilisez la[`InsertField`](../../aspose.words/documentbuilder/insertfield/) méthode .

### Exemples

Montre comment travailler avec une collection de champs.

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

    // Itérer sur la collection de champs et imprimer le contenu et le type
    // de chaque champ à l'aide d'une implémentation de visiteur personnalisée.
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
/// Documenter l'implémentation du visiteur qui imprime les informations de champ.
/// </summary>
public class FieldVisitor : DocumentVisitor
{
    public FieldVisitor()
    {
        mBuilder = new StringBuilder();
    }

    /// <summary>
    /// Obtient le texte brut du document qui a été accumulé par le visiteur.
    /// </summary>
    public string GetText()
    {
        return mBuilder.ToString();
    }

    /// <summary>
    /// Appelé lorsqu'un nœud FieldStart est rencontré dans le document.
    /// </summary>
    public override VisitorAction VisitFieldStart(FieldStart fieldStart)
    {
        mBuilder.AppendLine("Found field: " + fieldStart.FieldType);
        mBuilder.AppendLine("\tField code: " + fieldStart.GetField().GetFieldCode());
        mBuilder.AppendLine("\tDisplayed as: " + fieldStart.GetField().Result);

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Appelé lorsqu'un nœud FieldSeparator est rencontré dans le document.
    /// </summary>
    public override VisitorAction VisitFieldSeparator(FieldSeparator fieldSeparator)
    {
        mBuilder.AppendLine("\tFound separator: " + fieldSeparator.GetText());

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Appelé lorsqu'un nœud FieldEnd est rencontré dans le document.
    /// </summary>
    public override VisitorAction VisitFieldEnd(FieldEnd fieldEnd)
    {
        mBuilder.AppendLine("End of field: " + fieldEnd.FieldType);

        return VisitorAction.Continue;
    }

    private readonly StringBuilder mBuilder;
}
```

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

* class [FieldChar](../fieldchar/)
* espace de noms [Aspose.Words.Fields](../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
