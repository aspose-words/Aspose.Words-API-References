---
title: SdtType Enum
linktitle: SdtType
articleTitle: SdtType
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.Markup.SdtType, définissant des types de balises de documents structurés pour une gestion améliorée des documents et des flux de travail rationalisés.
type: docs
weight: 4730
url: /fr/net/aspose.words.markup/sdttype/
---
## SdtType enumeration

Spécifie le type d'un nœud de balise de document structuré (SDT).

```csharp
public enum SdtType
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| None | `0` | Aucun type n'est attribué au SDT. |
| Bibliography | `1` | Le SDT représente une entrée bibliographique. |
| Citation | `2` | Le SDT représente une citation. |
| Equation | `3` | Le SDT représente une équation. |
| DropDownList | `4` | Le SDT représente une liste déroulante lorsqu'il est affiché dans le document. |
| ComboBox | `5` | Le SDT représente une zone de liste déroulante lorsqu'il est affiché dans le document. |
| Date | `6` | Le SDT représente un sélecteur de date lorsqu'il est affiché dans le document. |
| BuildingBlockGallery | `7` | Le SDT représente un type de galerie de blocs de construction. |
| DocPartObj | `8` | Le SDT représente un type de partie de document. |
| Group | `9` | Le SDT représente un regroupement restreint lorsqu'il est affiché dans le document. |
| Picture | `10` | Le SDT représente une image lorsqu'il est affiché dans le document. |
| RichText | `11` | Le SDT représente une zone de texte enrichi lorsqu'il est affiché dans le document. |
| PlainText | `12` | Le SDT représente une zone de texte simple lorsqu'il est affiché dans le document. |
| Checkbox | `13` | Le SDT représente une case à cocher lorsqu'il est affiché dans le document. |
| RepeatingSection | `14` | Le SDT représente le type de section répétitive lorsqu'il est affiché dans le document. |
| RepeatingSectionItem | `15` | Le SDT représente un élément de section répétitif. |
| EntityPicker | `16` | Le SDT représente un sélecteur d'entités qui permet à l'utilisateur de sélectionner une instance d'un type de contenu externe. |

## Exemples

Montre comment créer une balise de document structurée de type Citation.

```csharp
Document doc = new Document();

StructuredDocumentTag sdt = new StructuredDocumentTag(doc, SdtType.Citation, MarkupLevel.Inline);
Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;
paragraph.AppendChild(sdt);

// Créer un champ Citation.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.MoveToParagraph(0, -1);
builder.InsertField(@"CITATION Ath22 \l 1033 ", "(John Lennon, 2022)");

// Déplacez le champ vers la balise de document structuré.
while (sdt.NextSibling != null)
    sdt.AppendChild(sdt.NextSibling);

doc.Save(ArtifactsDir + "StructuredDocumentTag.Citation.docx");
```

Montre comment créer une balise de document structurée en groupe au niveau de la ligne.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();

// Créez une balise de document structurée de groupe au niveau de la ligne.
StructuredDocumentTag groupSdt = new StructuredDocumentTag(doc, SdtType.Group, MarkupLevel.Row);
table.AppendChild(groupSdt);
groupSdt.IsShowingPlaceholderText = false;
groupSdt.RemoveAllChildren();

// Créer une ligne enfant de la balise de document structuré.
Row row = new Row(doc);
groupSdt.AppendChild(row);

Cell cell = new Cell(doc);
row.AppendChild(cell);

builder.EndTable();

// Insérer le contenu de la cellule.
cell.EnsureMinimum();
builder.MoveTo(cell.LastParagraph);
builder.Write("Lorem ipsum dolor.");

// Insérer du texte après le tableau.
builder.MoveTo(table.NextSibling);
builder.Write("Nulla blandit nisi.");

doc.Save(ArtifactsDir + "StructuredDocumentTag.SdtAtRowLevel.docx");
```

Montre comment travailler avec des styles pour les éléments de contrôle de contenu.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Vous trouverez ci-dessous deux manières d'appliquer un style du document à une balise de document structurée.
// 1 - Appliquer un objet de style de la collection de styles du document :
Style quoteStyle = doc.Styles[StyleIdentifier.Quote];
StructuredDocumentTag sdtPlainText =
    new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline) { Style = quoteStyle };

// 2 - Référencer un style dans le document par son nom :
StructuredDocumentTag sdtRichText =
    new StructuredDocumentTag(doc, SdtType.RichText, MarkupLevel.Inline) { StyleName = "Quote" };

builder.InsertNode(sdtPlainText);
builder.InsertNode(sdtRichText);

Assert.AreEqual(NodeType.StructuredDocumentTag, sdtPlainText.NodeType);

NodeCollection tags = doc.GetChildNodes(NodeType.StructuredDocumentTag, true);

foreach (Node node in tags)
{
    StructuredDocumentTag sdt = (StructuredDocumentTag)node;

    Console.WriteLine(sdt.WordOpenXMLMinimal);

    Assert.AreEqual(StyleIdentifier.Quote, sdt.Style.StyleIdentifier);
    Assert.AreEqual("Quote", sdt.StyleName);
}
```

Montre comment remplir un tableau avec des données provenant d'une partie XML.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

CustomXmlPart xmlPart = doc.CustomXmlParts.Add("Books",
    "<books>" +
        "<book>" +
            "<title>Everyday Italian</title>" +
            "<author>Giada De Laurentiis</author>" +
        "</book>" +
        "<book>" +
            "<title>The C Programming Language</title>" +
            "<author>Brian W. Kernighan, Dennis M. Ritchie</author>" +
        "</book>" +
        "<book>" +
            "<title>Learning XML</title>" +
            "<author>Erik T. Ray</author>" +
        "</book>" +
    "</books>");

// Créer des en-têtes pour les données à partir du contenu XML.
Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Title");
builder.InsertCell();
builder.Write("Author");
builder.EndRow();
builder.EndTable();

// Créez un tableau avec une section répétitive à l'intérieur.
StructuredDocumentTag repeatingSectionSdt =
    new StructuredDocumentTag(doc, SdtType.RepeatingSection, MarkupLevel.Row);
repeatingSectionSdt.XmlMapping.SetMapping(xmlPart, "/books[1]/book", string.Empty);
table.AppendChild(repeatingSectionSdt);

// Ajoutez un élément de section répétitif à l'intérieur de la section répétitive et marquez-le comme une ligne.
// Ce tableau aura une ligne pour chaque élément que nous pouvons trouver dans le document XML
// en utilisant le XPath "/books[1]/book", dont il existe trois.
StructuredDocumentTag repeatingSectionItemSdt =
    new StructuredDocumentTag(doc, SdtType.RepeatingSectionItem, MarkupLevel.Row);
repeatingSectionSdt.AppendChild(repeatingSectionItemSdt);

Row row = new Row(doc);
repeatingSectionItemSdt.AppendChild(row);

// Mappez les données XML avec les cellules de tableau créées pour le titre et l'auteur de chaque livre.
StructuredDocumentTag titleSdt =
    new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Cell);
titleSdt.XmlMapping.SetMapping(xmlPart, "/books[1]/book[1]/title[1]", string.Empty);
row.AppendChild(titleSdt);

StructuredDocumentTag authorSdt =
    new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Cell);
authorSdt.XmlMapping.SetMapping(xmlPart, "/books[1]/book[1]/author[1]", string.Empty);
row.AppendChild(authorSdt);

doc.Save(ArtifactsDir + "StructuredDocumentTag.RepeatingSectionItem.docx");
```

### Voir également

* espace de noms [Aspose.Words.Markup](../../aspose.words.markup/)
* Assemblée [Aspose.Words](../../)
