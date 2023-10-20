---
title: FormField Class
linktitle: FormField
articleTitle: FormField
second_title: Aspose.Words pour .NET
description: Aspose.Words.Fields.FormField classe. Représente un seul champ de formulaire en C#.
type: docs
weight: 2620
url: /fr/net/aspose.words.fields/formfield/
---
## FormField class

Représente un seul champ de formulaire.

Pour en savoir plus, visitez le[Travailler avec des champs de formulaire](https://docs.aspose.com/words/net/working-with-form-fields/) article documentaire.

```csharp
public class FormField : SpecialChar
```

## Propriétés

| Nom | La description |
| --- | --- |
| [CalculateOnExit](../../aspose.words.fields/formfield/calculateonexit/) { get; set; } | True si les références au champ de formulaire spécifié sont automatiquement mises à jour chaque fois que vous quittez le champ. |
| [CheckBoxSize](../../aspose.words.fields/formfield/checkboxsize/) { get; set; } | Obtient ou définit la taille de la case à cocher en points. N'a d'effet que lorsque[`IsCheckBoxExactSize`](./ischeckboxexactsize/) est`vrai` . |
| [Checked](../../aspose.words.fields/formfield/checked/) { get; set; } | Obtient ou définit l'état coché du champ du formulaire de case à cocher. La valeur par défaut de cette propriété est`FAUX` . |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Spécifie l'identifiant de nœud personnalisé. |
| [Default](../../aspose.words.fields/formfield/default/) { get; set; } | Obtient ou définit la valeur par défaut du champ du formulaire de case à cocher. La valeur par défaut de cette propriété est`FAUX` . |
| virtual [Document](../../aspose.words/node/document/) { get; } | Obtient le document auquel appartient ce nœud. |
| [DropDownItems](../../aspose.words.fields/formfield/dropdownitems/) { get; } | Permet d'accéder aux éléments d'un champ de formulaire déroulant. |
| [DropDownSelectedIndex](../../aspose.words.fields/formfield/dropdownselectedindex/) { get; set; } | Obtient ou définit l'index spécifiant l'élément actuellement sélectionné dans un champ de formulaire déroulant. |
| [Enabled](../../aspose.words.fields/formfield/enabled/) { get; set; } | Vrai si un champ de formulaire est activé. |
| [EntryMacro](../../aspose.words.fields/formfield/entrymacro/) { get; set; } | Renvoie ou définit un nom de macro d'entrée pour le champ du formulaire. |
| [ExitMacro](../../aspose.words.fields/formfield/exitmacro/) { get; set; } | Renvoie ou définit un nom de macro de sortie pour le champ du formulaire. |
| [Font](../../aspose.words/inline/font/) { get; } | Donne accès au formatage de la police de cet objet. |
| [HelpText](../../aspose.words.fields/formfield/helptext/) { get; set; } | Renvoie ou définit le texte affiché dans une boîte de message lorsque le champ du formulaire a le focus et que l'utilisateur appuie sur F1. |
| [IsCheckBoxExactSize](../../aspose.words.fields/formfield/ischeckboxexactsize/) { get; set; } | Obtient ou définit la valeur booléenne qui indique si la taille de la zone de texte est automatique ou spécifiée explicitement. |
| virtual [IsComposite](../../aspose.words/node/iscomposite/) { get; } | Retours`vrai` si ce nœud peut contenir d'autres nœuds. |
| [IsDeleteRevision](../../aspose.words/inline/isdeleterevision/) { get; } | Renvoie vrai si cet objet a été supprimé dans Microsoft Word alors que le suivi des modifications était activé. |
| [IsFormatRevision](../../aspose.words/inline/isformatrevision/) { get; } | Renvoie vrai si le formatage de l'objet a été modifié dans Microsoft Word alors que le suivi des modifications était activé. |
| [IsInsertRevision](../../aspose.words/inline/isinsertrevision/) { get; } | Renvoie vrai si cet objet a été inséré dans Microsoft Word alors que le suivi des modifications était activé. |
| [IsMoveFromRevision](../../aspose.words/inline/ismovefromrevision/) { get; } | Retours`vrai` si cet objet a été déplacé (supprimé) dans Microsoft Word alors que le suivi des modifications était activé. |
| [IsMoveToRevision](../../aspose.words/inline/ismovetorevision/) { get; } | Retours`vrai` si cet objet a été déplacé (inséré) dans Microsoft Word alors que le suivi des modifications était activé. |
| [MaxLength](../../aspose.words.fields/formfield/maxlength/) { get; set; } | Longueur maximale du champ de texte. Zéro lorsque la longueur n'est pas limitée. |
| [Name](../../aspose.words.fields/formfield/name/) { get; set; } | Obtient ou définit le nom du champ du formulaire. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Obtient le nœud suivant immédiatement ce nœud. |
| override [NodeType](../../aspose.words.fields/formfield/nodetype/) { get; } | RetoursFormField . |
| [OwnHelp](../../aspose.words.fields/formfield/ownhelp/) { get; set; } | Spécifie la source du texte affiché dans une boîte de message lorsqu'un champ de formulaire a le focus et que l'utilisateur appuie sur F1. |
| [OwnStatus](../../aspose.words.fields/formfield/ownstatus/) { get; set; } | Spécifie la source du texte affiché dans la barre d'état lorsqu'un champ de formulaire a le focus. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Obtient le parent immédiat de ce nœud. |
| [ParentParagraph](../../aspose.words/inline/parentparagraph/) { get; } | Récupère le parent[`Paragraph`](../../aspose.words/paragraph/) de ce nœud. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Obtient le nœud précédant immédiatement ce nœud. |
| [Range](../../aspose.words/node/range/) { get; } | Renvoie un[`Range`](../../aspose.words/range/) objet qui représente la partie d'un document contenue dans ce nœud. |
| [Result](../../aspose.words.fields/formfield/result/) { get; set; } | Obtient ou définit une chaîne qui représente le résultat de ce champ de formulaire. |
| [StatusText](../../aspose.words.fields/formfield/statustext/) { get; set; } | Renvoie ou définit le texte affiché dans la barre d'état lorsqu'un champ de formulaire a le focus. |
| [TextInputDefault](../../aspose.words.fields/formfield/textinputdefault/) { get; set; } | Obtient ou définit la chaîne par défaut ou une expression de calcul d'un champ de formulaire de texte. |
| [TextInputFormat](../../aspose.words.fields/formfield/textinputformat/) { get; set; } | Renvoie ou définit la mise en forme du texte pour un champ de formulaire de texte. |
| [TextInputType](../../aspose.words.fields/formfield/textinputtype/) { get; set; } | Obtient ou définit le type d'un champ de formulaire de texte. |
| [Type](../../aspose.words.fields/formfield/type/) { get; } | Renvoie le type de champ du formulaire. |

## Méthodes

| Nom | La description |
| --- | --- |
| override [Accept](../../aspose.words.fields/formfield/accept/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Accepte un visiteur. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Crée un duplicata du nœud. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../../aspose.words/nodetype/)*) | Obtient le premier ancêtre du spécifié[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Obtient le premier ancêtre du type d'objet spécifié. |
| override [GetText](../../aspose.words/specialchar/gettext/)() | Obtient le caractère spécial que représente ce nœud. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../../aspose.words/node/)*) | Obtient le nœud suivant selon l'algorithme de traversée de l'arbre de pré-commande. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../../aspose.words/node/)*) | Obtient le nœud précédent selon l'algorithme de traversée d'arbre de pré-commande. |
| [Remove](../../aspose.words/node/remove/)() | Se supprime du parent. |
| [RemoveField](../../aspose.words.fields/formfield/removefield/)() | Supprime le champ de formulaire complet, pas seulement le caractère spécial du champ de formulaire. |
| [SetTextInputValue](../../aspose.words.fields/formfield/settextinputvalue/)(*object*) | Applique le format de texte spécifié dans[`TextInputFormat`](./textinputformat/) et stocke la valeur dans[`Result`](./result/) . |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../../aspose.words/saveformat/)*) | Exporte le contenu du nœud dans une chaîne au format spécifié. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Exporte le contenu du nœud dans une chaîne à l'aide des options de sauvegarde spécifiées. |

## Remarques

Microsoft Word fournit les champs de formulaire suivants : case à cocher, saisie de texte et liste déroulante (liste déroulante).

`FormField`est un nœud en ligne et ne peut être qu'un enfant de[`Paragraph`](../../aspose.words/paragraph/).

`FormField` est représenté dans un document par un caractère spécial et positionné comme un caractère dans une ligne de texte.

Un champ de formulaire complet dans un document Word est une structure complexe représentée par plusieurs nœuds : début du champ, code de champ tel que FORMTEXT, données du champ de formulaire, séparateur de champ, résultat du champ , fin du champ et un signet. Pour créer par programme des champs de formulaire dans un document Word, use [`InsertCheckBox`](../../aspose.words/documentbuilder/insertcheckbox/) , [`InsertTextInput`](../../aspose.words/documentbuilder/inserttextinput/) et [`InsertComboBox`](../../aspose.words/documentbuilder/insertcombobox/) which assurez-vous que tous les nœuds du champ de formulaire sont créés dans le bon ordre et dans un état approprié.

## Exemples

Montre comment formater l'intégralité du FormField, y compris la valeur du champ.

```csharp
Document doc = new Document(MyDir + "Form fields.docx");

FormField formField = doc.Range.FormFields[0];
formField.Font.Bold = true;
formField.Font.Size = 24;
formField.Font.Color = Color.Red;

formField.Result = "Aspose.FormField";

doc = DocumentHelper.SaveOpen(doc);

Run formFieldRun = doc.FirstSection.Body.FirstParagraph.Runs[1];

Assert.AreEqual("Aspose.FormField", formFieldRun.Text);
Assert.AreEqual(true, formFieldRun.Font.Bold);
Assert.AreEqual(24, formFieldRun.Font.Size);
Assert.AreEqual(Color.Red.ToArgb(), formFieldRun.Font.Color.ToArgb());
```

Montre comment insérer une zone de liste déroulante.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Please select a fruit: ");

// Insère une zone de liste déroulante qui permettra à un utilisateur de choisir une option parmi une collection de chaînes.
FormField comboBox = builder.InsertComboBox("MyComboBox", new[] { "Apple", "Banana", "Cherry" }, 0);

Assert.AreEqual("MyComboBox", comboBox.Name);
Assert.AreEqual(FieldType.FieldFormDropDown, comboBox.Type);
Assert.AreEqual("Apple", comboBox.Result);

// Le champ du formulaire apparaîtra sous la forme d'une balise html "select".
doc.Save(ArtifactsDir + "FormFields.Create.html");
```

### Voir également

* class [SpecialChar](../../aspose.words/specialchar/)
* espace de noms [Aspose.Words.Fields](../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../)
