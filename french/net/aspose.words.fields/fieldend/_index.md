---
title: FieldEnd
second_title: Référence de l'API Aspose.Words pour .NET
description: Représente la fin dun champ Word dans un document.
type: docs
weight: 1710
url: /fr/net/aspose.words.fields/fieldend/
---
## FieldEnd class

Représente la fin d'un champ Word dans un document.

```csharp
public class FieldEnd : FieldChar
```

## Propriétés

| Nom | La description |
| --- | --- |
| [CustomNodeId](../../aspose.words/node/customnodeid) { get; set; } | Spécifie l'identifiant de nœud personnalisé. |
| virtual [Document](../../aspose.words/node/document) { get; } | Obtient le document auquel ce nœud appartient. |
| [FieldType](../../aspose.words.fields/fieldchar/fieldtype) { get; } | Renvoie le type du champ. |
| [Font](../../aspose.words/inline/font) { get; } | Fournit l'accès à la mise en forme de la police de cet objet. |
| [HasSeparator](../../aspose.words.fields/fieldend/hasseparator) { get; } | Retours **vrai** si ce champ a un séparateur. |
| virtual [IsComposite](../../aspose.words/node/iscomposite) { get; } | Renvoie true si ce nœud peut contenir d'autres nœuds. |
| [IsDeleteRevision](../../aspose.words/inline/isdeleterevision) { get; } | Renvoie true si cet objet a été supprimé dans Microsoft Word alors que le suivi des modifications était activé. |
| [IsDirty](../../aspose.words.fields/fieldchar/isdirty) { get; set; } | Obtient ou définit si le résultat actuel du champ n'est plus correct (périmé) en raison d'autres modifications apportées au document. |
| [IsFormatRevision](../../aspose.words/inline/isformatrevision) { get; } | Renvoie true si la mise en forme de l'objet a été modifiée dans Microsoft Word alors que le suivi des modifications était activé. |
| [IsInsertRevision](../../aspose.words/inline/isinsertrevision) { get; } | Renvoie true si cet objet a été inséré dans Microsoft Word alors que le suivi des modifications était activé. |
| [IsLocked](../../aspose.words.fields/fieldchar/islocked) { get; set; } | Obtient ou définit si le champ parent est verrouillé (ne doit pas recalculer son résultat). |
| [IsMoveFromRevision](../../aspose.words/inline/ismovefromrevision) { get; } | Retours **vrai** si cet objet a été déplacé (supprimé) dans Microsoft Word alors que le suivi des modifications était activé. |
| [IsMoveToRevision](../../aspose.words/inline/ismovetorevision) { get; } | Retours **vrai** si cet objet a été déplacé (inséré) dans Microsoft Word alors que le suivi des modifications était activé. |
| [NextSibling](../../aspose.words/node/nextsibling) { get; } | Obtient le nœud suivant immédiatement ce nœud. |
| override [NodeType](../../aspose.words.fields/fieldend/nodetype) { get; } | RetoursFieldEnd . |
| [ParentNode](../../aspose.words/node/parentnode) { get; } | Obtient le parent immédiat de ce nœud. |
| [ParentParagraph](../../aspose.words/inline/parentparagraph) { get; } | Récupère le parent[`Paragraph`](../../aspose.words/paragraph) de ce nœud. |
| [PreviousSibling](../../aspose.words/node/previoussibling) { get; } | Obtient le nœud précédant immédiatement ce nœud. |
| [Range](../../aspose.words/node/range) { get; } | Renvoie un **Intervalle** objet qui représente la partie d'un document contenue dans ce nœud. |

## Méthodes

| Nom | La description |
| --- | --- |
| override [Accept](../../aspose.words.fields/fieldend/accept)(DocumentVisitor) | Accepte un visiteur. |
| [Clone](../../aspose.words/node/clone)(bool) | Crée un doublon du nœud. |
| [GetAncestor](../../aspose.words/node/getancestor)(NodeType) | Obtient le premier ancêtre du spécifié[`NodeType`](../../aspose.words/nodetype) . |
| [GetAncestor](../../aspose.words/node/getancestor)(Type) | Obtient le premier ancêtre du type d'objet spécifié. |
| [GetField](../../aspose.words.fields/fieldchar/getfield)() | Renvoie un champ pour le champ car. |
| override [GetText](../../aspose.words/specialchar/gettext)() | Obtient le caractère spécial que ce nœud représente. |
| [NextPreOrder](../../aspose.words/node/nextpreorder)(Node) | Obtient le nœud suivant selon l'algorithme de traversée de l'arbre de pré-ordre. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder)(Node) | Obtient le nœud précédent selon l'algorithme de parcours de l'arbre de pré-ordre. |
| [Remove](../../aspose.words/node/remove)() | Se supprime du parent. |
| [ToString](../../aspose.words/node/tostring)(SaveFormat) | Exporte le contenu du nœud dans une chaîne au format spécifié. |
| [ToString](../../aspose.words/node/tostring)(SaveOptions) | Exporte le contenu du nœud dans une chaîne à l'aide des options d'enregistrement spécifiées. |

### Remarques

[`FieldEnd`](../fieldend) est un nœud de niveau en ligne et représenté par le[`FieldEndChar`](../../aspose.words/controlchar/fieldendchar) caractère de contrôle dans le document.

[`FieldEnd`](../fieldend) ne peut être qu'un enfant de[`Paragraph`](../../aspose.words/paragraph).

Un champ complet dans un document Microsoft Word est une structure complexe composée de un caractère de début de champ, un code de champ, un caractère séparateur de champ, un résultat de champ et un caractère de fin de champ. Certains champs n'ont qu'un début de champ, un code de champ et une fin de champ.

Pour insérer facilement un nouveau champ dans un document, utilisez la[`InsertField`](../../aspose.words/documentbuilder/insertfield) méthode .

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

### Voir également

* class [FieldChar](../fieldchar)
* espace de noms [Aspose.Words.Fields](../../aspose.words.fields)
* Assemblée [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
