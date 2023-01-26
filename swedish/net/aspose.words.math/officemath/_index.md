---
title: OfficeMath
second_title: Aspose.Words för .NET API Referens
description: Representerar ett Office Mathobjekt som funktion ekvation matris eller liknande. Kan innehålla underordnade elements inklusive körningar av matematisk text bokmärken kommentarer annatOfficeMath./officemath/ instanser och några andra noder.
type: docs
weight: 3880
url: /sv/net/aspose.words.math/officemath/
---
## OfficeMath class

Representerar ett Office Math-objekt som funktion, ekvation, matris eller liknande. Kan innehålla underordnade elements inklusive körningar av matematisk text, bokmärken, kommentarer, annat`OfficeMath` instanser och några andra noder.

```csharp
public class OfficeMath : CompositeNode
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [ChildNodes](../../aspose.words/compositenode/childnodes/) { get; } | Hämtar alla omedelbara underordnade noder för denna nod. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Hämtar antalet omedelbara barn till denna nod. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Anger anpassad nodidentifierare. |
| [DisplayType](../../aspose.words.math/officemath/displaytype/) { get; set; } | Hämtar/ställer in Office Math visningsformattyp som representerar om en ekvation visas inline med texten eller visas på sin egen rad. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Hämtar dokumentet som denna nod tillhör. |
| [EquationXmlEncoding](../../aspose.words.math/officemath/equationxmlencoding/) { get; set; } | Hämtar/ställer in en kodning som användes för att koda ekvations-XML, om detta matematiska kontorsobjekt läses från -ekvations-XML. Vi använder kodningen när vi sparar ett dokument för att skriva i samma kodning som det lästes. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Får det första barnet i noden. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Returnerar sant om denna nod har några underordnade noder. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Returnerar sant eftersom denna nod kan ha underordnade noder. |
| [Justification](../../aspose.words.math/officemath/justification/) { get; set; } | Får/ställer in Office Math motivering. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Hämtar nodens sista underordnade. |
| [MathObjectType](../../aspose.words.math/officemath/mathobjecttype/) { get; } | Får typ[`MathObjectType`](./mathobjecttype/) av detta Office Math-objekt. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Hämtar noden omedelbart efter denna nod. |
| override [NodeType](../../aspose.words.math/officemath/nodetype/) { get; } | Returnerar **NodeType.OfficeMath** . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Hämtar den omedelbara föräldern till denna nod. |
| [ParentParagraph](../../aspose.words.math/officemath/parentparagraph/) { get; } | Hämtar föräldern[`Paragraph`](../../aspose.words/paragraph/) av denna nod. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Hämtar noden omedelbart före denna nod. |
| [Range](../../aspose.words/node/range/) { get; } | Returnerar en **Räckvidd** objekt som representerar den del av ett dokument som finns i denna nod. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| override [Accept](../../aspose.words.math/officemath/accept/)(DocumentVisitor) | Accepterar en besökare. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(Node) | Lägger till den angivna noden i slutet av listan över underordnade noder för denna nod. |
| [Clone](../../aspose.words/node/clone/)(bool) | Skapar en dubblett av noden. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Reserverad för systemanvändning. IXPathNavigable. |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | Hämtar den första förfadern till den angivna[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | Hämtar den första förfadern till den angivna objekttypen. |
| [GetChild](../../aspose.words/compositenode/getchild/)(NodeType, int, bool) | Returnerar en N:te underordnad nod som matchar den angivna typen. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(NodeType, bool) | Returnerar en aktiv samling av underordnade noder som matchar den angivna typen. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Tillhandahåller stöd för varje stiliteration över undernoderna för denna nod. |
| [GetMathRenderer](../../aspose.words.math/officemath/getmathrenderer/)() | Skapar och returnerar ett objekt som kan användas för att rendera denna ekvation till en bild. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Hämtar texten för denna nod och alla dess underordnade. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(Node) | Returnerar indexet för den angivna undernoden i den underordnade nodmatrisen. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(Node, Node) | Infogar den angivna noden omedelbart efter den angivna referensnoden. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(Node, Node) | Infogar den angivna noden omedelbart före den angivna referensnoden. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | Hämtar nästa nod enligt algoritmen för förbeställningsträdet. |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(Node) | Lägger till den angivna noden i början av listan över underordnade noder för denna nod. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(Node) | Hämtar föregående nod enligt algoritmen för förbeställningsträdet. |
| [Remove](../../aspose.words/node/remove/)() | Tar bort sig själv från föräldern. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Tar bort alla undernoder för den aktuella noden. |
| [RemoveChild](../../aspose.words/compositenode/removechild/)(Node) | Tar bort den angivna underordnade noden. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Tar bort alla[`SmartTag`](../../aspose.words.markup/smarttag/) underliggande noder till den aktuella noden. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(string) | Väljer en lista med noder som matchar XPath-uttrycket. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(string) | Väljer den första noden som matchar XPath-uttrycket. |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | Exporterar innehållet i noden till en sträng i angivet format. |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | Exporterar innehållet i noden till en sträng med de angivna sparalternativen. |

### Anmärkningar

I den här versionen av Aspose.Words,`OfficeMath` noder tillhandahåller inte public methods och egenskaper för att skapa eller ändra ett OfficeMath-objekt. I den här versionen kan du inte instansiera Math noder eller ändra befintliga förutom att ta bort dem.

`OfficeMath` kan bara vara ett barn av[`Paragraph`](../../aspose.words/paragraph/).

### Exempel

Visar hur du ställer in kontorsmattevisningsformatering.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath officeMath = (OfficeMath) doc.GetChild(NodeType.OfficeMath, 0, true);

// OfficeMath-noder som är barn till andra OfficeMath-noder är alltid inline.
// Noden vi arbetar med är basnoden för att ändra dess plats och visningstyp.
Assert.AreEqual(MathObjectType.OMathPara, officeMath.MathObjectType);
Assert.AreEqual(NodeType.OfficeMath, officeMath.NodeType);
Assert.AreEqual(officeMath.ParentNode, officeMath.ParentParagraph);

// OOXML- och WML-format använder egenskapen "EquationXmlEncoding".
Assert.IsNull(officeMath.EquationXmlEncoding);

// Ändra plats och visningstyp för OfficeMath-noden.
officeMath.DisplayType = OfficeMathDisplayType.Display;
officeMath.Justification = OfficeMathJustification.Left;

doc.Save(ArtifactsDir + "Shape.OfficeMath.docx");
```

### Se även

* class [CompositeNode](../../aspose.words/compositenode/)
* namnutrymme [Aspose.Words.Math](../../aspose.words.math/)
* hopsättning [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
