---
title: NonBreakingHyphenChar
second_title: Référence de l'API Aspose.Words pour .NET
description: Le trait dunion insécable dans Microsoft Word est char30.
type: docs
weight: 160
url: /fr/net/aspose.words/controlchar/nonbreakinghyphenchar/
---
## ControlChar.NonBreakingHyphenChar field

Le trait d'union insécable dans Microsoft Word est (char)30.

```csharp
public const char NonBreakingHyphenChar;
```

### Remarques

Le trait d'union insécable dans Microsoft Word ne correspond pas au trait d'union insécable du caractère Unicode U+2011, mais représente à la place des informations internes qui indiquent à Microsoft Word d'afficher un trait d'union et de ne pas couper de ligne.

Informations utiles : http://www.cs.tut.fi/~jkorpela/dashes.html#linebreaks.

### Exemples

Montre comment ajouter divers caractères de contrôle à un document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ajoute un espace normal.
builder.Write("Before space." + ControlChar.SpaceChar + "After space.");

// Ajoutez un NBSP, qui est un espace insécable.
// Contrairement à l'espace normal, cet espace ne peut pas avoir de saut de ligne automatique à sa position.
builder.Write("Before space." + ControlChar.NonBreakingSpace + "After space.");

// Ajoute un caractère de tabulation.
builder.Write("Before tab." + ControlChar.Tab + "After tab.");

// Ajoute un saut de ligne.
builder.Write("Before line break." + ControlChar.LineBreak + "After line break.");

// Ajoute une nouvelle ligne et commence un nouveau paragraphe.
Assert.AreEqual(1, doc.FirstSection.Body.GetChildNodes(NodeType.Paragraph, true).Count);
builder.Write("Before line feed." + ControlChar.LineFeed + "After line feed.");
Assert.AreEqual(2, doc.FirstSection.Body.GetChildNodes(NodeType.Paragraph, true).Count);

// Le caractère de saut de ligne a deux versions.
Assert.AreEqual(ControlChar.LineFeed, ControlChar.Lf);

// Les retours chariot et les sauts de ligne peuvent être représentés ensemble par un seul caractère.
Assert.AreEqual(ControlChar.CrLf, ControlChar.Cr + ControlChar.Lf);

// Ajoute un saut de paragraphe, qui commencera un nouveau paragraphe.
builder.Write("Before paragraph break." + ControlChar.ParagraphBreak + "After paragraph break.");
Assert.AreEqual(3, doc.FirstSection.Body.GetChildNodes(NodeType.Paragraph, true).Count);

// Ajoute un saut de section. Cela ne crée pas une nouvelle section ou un nouveau paragraphe.
Assert.AreEqual(1, doc.Sections.Count);
builder.Write("Before section break." + ControlChar.SectionBreak + "After section break.");
Assert.AreEqual(1, doc.Sections.Count);

// Ajoute un saut de page.
builder.Write("Before page break." + ControlChar.PageBreak + "After page break.");

// Un saut de page a la même valeur qu'un saut de section.
Assert.AreEqual(ControlChar.PageBreak, ControlChar.SectionBreak);

// Insère une nouvelle section, puis définit son nombre de colonnes sur deux.
doc.AppendChild(new Section(doc));
builder.MoveToSection(1);
builder.CurrentSection.PageSetup.TextColumns.SetCount(2);

// Nous pouvons utiliser un caractère de contrôle pour marquer le point où le texte passe à la colonne suivante.
builder.Write("Text at end of column 1." + ControlChar.ColumnBreak + "Text at beginning of column 2.");

doc.Save(ArtifactsDir + "ControlChar.InsertControlChars.docx");

// Il existe des équivalents char et string pour la plupart des caractères.
Assert.AreEqual(Convert.ToChar(ControlChar.Cell), ControlChar.CellChar);
Assert.AreEqual(Convert.ToChar(ControlChar.NonBreakingSpace), ControlChar.NonBreakingSpaceChar);
Assert.AreEqual(Convert.ToChar(ControlChar.Tab), ControlChar.TabChar);
Assert.AreEqual(Convert.ToChar(ControlChar.LineBreak), ControlChar.LineBreakChar);
Assert.AreEqual(Convert.ToChar(ControlChar.LineFeed), ControlChar.LineFeedChar);
Assert.AreEqual(Convert.ToChar(ControlChar.ParagraphBreak), ControlChar.ParagraphBreakChar);
Assert.AreEqual(Convert.ToChar(ControlChar.SectionBreak), ControlChar.SectionBreakChar);
Assert.AreEqual(Convert.ToChar(ControlChar.PageBreak), ControlChar.SectionBreakChar);
Assert.AreEqual(Convert.ToChar(ControlChar.ColumnBreak), ControlChar.ColumnBreakChar);
```

### Voir également

* class [ControlChar](../../controlchar)
* espace de noms [Aspose.Words](../../controlchar)
* Assemblée [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->