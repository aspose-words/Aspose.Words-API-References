---
title: FormField Class
linktitle: FormField
articleTitle: FormField
second_title: Aspose.Words för .NET
description: Aspose.Words.Fields.FormField klass. Representerar ett enda formulärfält i C#.
type: docs
weight: 2620
url: /sv/net/aspose.words.fields/formfield/
---
## FormField class

Representerar ett enda formulärfält.

För att lära dig mer, besök[Arbeta med formulärfält](https://docs.aspose.com/words/net/working-with-form-fields/) dokumentationsartikel.

```csharp
public class FormField : SpecialChar
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [CalculateOnExit](../../aspose.words.fields/formfield/calculateonexit/) { get; set; } | Sant om referenser till det angivna formulärfältet uppdateras automatiskt när fältet avslutas. |
| [CheckBoxSize](../../aspose.words.fields/formfield/checkboxsize/) { get; set; } | Hämtar eller ställer in storleken på kryssrutan i poäng. Har effekt endast när[`IsCheckBoxExactSize`](./ischeckboxexactsize/) är`Sann` . |
| [Checked](../../aspose.words.fields/formfield/checked/) { get; set; } | Hämtar eller ställer in den markerade statusen för kryssrutans formulärfält. Standardvärdet för den här egenskapen är`falsk` . |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Anger anpassad nodidentifierare. |
| [Default](../../aspose.words.fields/formfield/default/) { get; set; } | Hämtar eller ställer in standardvärdet för kryssrutans formulärfält. Standardvärdet för den här egenskapen är`falsk` . |
| virtual [Document](../../aspose.words/node/document/) { get; } | Hämtar dokumentet som denna nod tillhör. |
| [DropDownItems](../../aspose.words.fields/formfield/dropdownitems/) { get; } | Ger tillgång till objekten i ett rullgardinsformulärfält. |
| [DropDownSelectedIndex](../../aspose.words.fields/formfield/dropdownselectedindex/) { get; set; } | Hämtar eller ställer in indexet som anger det för närvarande valda objektet i ett rullgardinsfält. |
| [Enabled](../../aspose.words.fields/formfield/enabled/) { get; set; } | True om ett formulärfält är aktiverat. |
| [EntryMacro](../../aspose.words.fields/formfield/entrymacro/) { get; set; } | Returnerar eller ställer in ett postmakronamn för formulärfältet. |
| [ExitMacro](../../aspose.words.fields/formfield/exitmacro/) { get; set; } | Returnerar eller ställer in ett utgångsmakronamn för formulärfältet. |
| [Font](../../aspose.words/inline/font/) { get; } | Ger tillgång till teckensnittsformateringen för detta objekt. |
| [HelpText](../../aspose.words.fields/formfield/helptext/) { get; set; } | Returnerar eller ställer in texten som visas i en meddelanderuta när formulärfältet har fokus och användaren trycker på F1. |
| [IsCheckBoxExactSize](../../aspose.words.fields/formfield/ischeckboxexactsize/) { get; set; } | Hämtar eller ställer in det booleska värdet som indikerar om storleken på textrutan är automatisk eller specificerad explicit. |
| virtual [IsComposite](../../aspose.words/node/iscomposite/) { get; } | Returnerar`Sann` om denna nod kan innehålla andra noder. |
| [IsDeleteRevision](../../aspose.words/inline/isdeleterevision/) { get; } | Returnerar sant om detta objekt raderades i Microsoft Word medan ändringsspårning var aktiverad. |
| [IsFormatRevision](../../aspose.words/inline/isformatrevision/) { get; } | Returnerar sant om formateringen av objektet ändrades i Microsoft Word medan ändringsspårning var aktiverad. |
| [IsInsertRevision](../../aspose.words/inline/isinsertrevision/) { get; } | Returnerar sant om det här objektet infogades i Microsoft Word medan ändringsspårning var aktiverad. |
| [IsMoveFromRevision](../../aspose.words/inline/ismovefromrevision/) { get; } | Returnerar`Sann` om det här objektet flyttades (borttogs) i Microsoft Word medan ändringsspårning var aktiverad. |
| [IsMoveToRevision](../../aspose.words/inline/ismovetorevision/) { get; } | Returnerar`Sann` om detta objekt flyttades (infogades) i Microsoft Word medan ändringsspårning var aktiverad. |
| [MaxLength](../../aspose.words.fields/formfield/maxlength/) { get; set; } | Maximal längd för textfältet. Noll när längden inte är begränsad. |
| [Name](../../aspose.words.fields/formfield/name/) { get; set; } | Hämtar eller ställer in formulärfältets namn. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Hämtar noden omedelbart efter denna nod. |
| override [NodeType](../../aspose.words.fields/formfield/nodetype/) { get; } | ReturnerarFormField . |
| [OwnHelp](../../aspose.words.fields/formfield/ownhelp/) { get; set; } | Anger källan till texten som visas i en meddelanderuta när ett formulärfält har fokus och användaren trycker på F1. |
| [OwnStatus](../../aspose.words.fields/formfield/ownstatus/) { get; set; } | Anger källan till texten som visas i statusfältet när ett formulärfält har fokus. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Hämtar den omedelbara föräldern till denna nod. |
| [ParentParagraph](../../aspose.words/inline/parentparagraph/) { get; } | Hämtar föräldern[`Paragraph`](../../aspose.words/paragraph/) av denna nod. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Hämtar noden omedelbart före denna nod. |
| [Range](../../aspose.words/node/range/) { get; } | Returnerar en[`Range`](../../aspose.words/range/) objekt som representerar den del av ett dokument som finns i denna nod. |
| [Result](../../aspose.words.fields/formfield/result/) { get; set; } | Hämtar eller ställer in en sträng som representerar resultatet av detta formulärfält. |
| [StatusText](../../aspose.words.fields/formfield/statustext/) { get; set; } | Returnerar eller ställer in texten som visas i statusfältet när ett formulärfält har fokus. |
| [TextInputDefault](../../aspose.words.fields/formfield/textinputdefault/) { get; set; } | Hämtar eller ställer in standardsträngen eller ett beräkningsuttryck för ett textformulärfält. |
| [TextInputFormat](../../aspose.words.fields/formfield/textinputformat/) { get; set; } | Returnerar eller ställer in textformateringen för ett textformulärfält. |
| [TextInputType](../../aspose.words.fields/formfield/textinputtype/) { get; set; } | Hämtar eller ställer in typen av ett textformulärfält. |
| [Type](../../aspose.words.fields/formfield/type/) { get; } | Returnerar formulärfältstypen. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| override [Accept](../../aspose.words.fields/formfield/accept/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Accepterar en besökare. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Skapar en dubblett av noden. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../../aspose.words/nodetype/)*) | Hämtar den första förfadern till den angivna[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Hämtar den första förfadern till den angivna objekttypen. |
| override [GetText](../../aspose.words/specialchar/gettext/)() | Får specialtecknet som denna nod representerar. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../../aspose.words/node/)*) | Hämtar nästa nod enligt algoritmen för förbeställningsträdet. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../../aspose.words/node/)*) | Hämtar föregående nod enligt algoritmen för förbeställningsträdet. |
| [Remove](../../aspose.words/node/remove/)() | Tar bort sig själv från föräldern. |
| [RemoveField](../../aspose.words.fields/formfield/removefield/)() | Tar bort hela formulärfältet, inte bara formulärfältets specialtecken. |
| [SetTextInputValue](../../aspose.words.fields/formfield/settextinputvalue/)(*object*) | Tillämpar textformatet som anges i[`TextInputFormat`](./textinputformat/) och lagrar värdet i[`Result`](./result/) . |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../../aspose.words/saveformat/)*) | Exporterar innehållet i noden till en sträng i angivet format. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Exporterar innehållet i noden till en sträng med de angivna sparalternativen. |

## Anmärkningar

Microsoft Word tillhandahåller följande formulärfält: kryssruta, textinmatning och rullgardinsmeny (kombobox).

`FormField`är en inline-nod och kan bara vara ett barn till[`Paragraph`](../../aspose.words/paragraph/).

`FormField` representeras i ett dokument av ett specialtecken och placerat som ett tecken inom en textrad.

Ett komplett formulärfält i ett Word-dokument är en komplex struktur som representeras av flera noder: fältstart, fältkod som FORMTEXT, formulärfältsdata, fältavgränsare, fältresultat, fältslut och ett bokmärke. För att programmatiskt skapa formulärfält i ett Word-dokument use [`InsertCheckBox`](../../aspose.words/documentbuilder/insertcheckbox/) , [`InsertTextInput`](../../aspose.words/documentbuilder/inserttextinput/) och [`InsertComboBox`](../../aspose.words/documentbuilder/insertcombobox/) which se till att alla formulärfältsnoder skapas i rätt ordning och i lämpligt tillstånd.

## Exempel

Visar hur man formaterar hela FormField, inklusive fältvärdet.

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

Visar hur man infogar en kombinationsruta.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Please select a fruit: ");

// Infoga en kombinationsruta som låter en användare välja ett alternativ från en samling strängar.
FormField comboBox = builder.InsertComboBox("MyComboBox", new[] { "Apple", "Banana", "Cherry" }, 0);

Assert.AreEqual("MyComboBox", comboBox.Name);
Assert.AreEqual(FieldType.FieldFormDropDown, comboBox.Type);
Assert.AreEqual("Apple", comboBox.Result);

// Formulärfältet kommer att visas i form av en "select" html-tagg.
doc.Save(ArtifactsDir + "FormFields.Create.html");
```

### Se även

* class [SpecialChar](../../aspose.words/specialchar/)
* namnutrymme [Aspose.Words.Fields](../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../)
