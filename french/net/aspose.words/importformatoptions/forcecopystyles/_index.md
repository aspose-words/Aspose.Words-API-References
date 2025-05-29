---
title: ImportFormatOptions.ForceCopyStyles
linktitle: ForceCopyStyles
articleTitle: ForceCopyStyles
second_title: Aspose.Words pour .NET
description: Découvrez la propriété ForceCopyStyles d'ImportFormatOptions pour contrôler facilement la copie des styles en mode KeepSourceFormatting. La valeur par défaut est « false » pour des résultats optimaux.
type: docs
weight: 30
url: /fr/net/aspose.words/importformatoptions/forcecopystyles/
---
## ImportFormatOptions.ForceCopyStyles property

Obtient ou définit une valeur booléenne indiquant de copier les styles conflictuels dansKeepSourceFormatting mode. La valeur par défaut est`FAUX` .

```csharp
public bool ForceCopyStyles { get; set; }
```

## Remarques

Par défaut, si un style correspondant existe déjà dans un document de destination, le style source formatting est développé en attributs de nœud directs et le style de ce nœud est réinitialisé à une valeur par défaut.

Lorsque cette option est définie sur`vrai`, le style source sera copié de force dans le document de destination avec un nom unique et appliqué au nœud importé.

Attention, dans ce cas, il n'est pas garanti que le formatage du nœud importé dans le document de destination soit conservé.

## Exemples

Montre comment copier de force des styles sources avec des noms uniques.

```csharp
// Les deux documents contiennent MyStyle1 et MyStyle2, MyStyle3 existe uniquement dans un document source.
Document srcDoc = new Document(MyDir + "Styles source.docx");
Document dstDoc = new Document(MyDir + "Styles destination.docx");

ImportFormatOptions options = new ImportFormatOptions { ForceCopyStyles = true };
dstDoc.AppendDocument(srcDoc, ImportFormatMode.KeepSourceFormatting, options);

ParagraphCollection paras = dstDoc.Sections[1].Body.Paragraphs;

Assert.AreEqual(paras[0].ParagraphFormat.Style.Name, "MyStyle1_0");
Assert.AreEqual(paras[1].ParagraphFormat.Style.Name, "MyStyle2_0");
Assert.AreEqual(paras[2].ParagraphFormat.Style.Name, "MyStyle3");
```

### Voir également

* class [ImportFormatOptions](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
