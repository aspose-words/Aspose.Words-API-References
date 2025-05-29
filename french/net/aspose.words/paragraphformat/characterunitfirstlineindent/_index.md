---
title: ParagraphFormat.CharacterUnitFirstLineIndent
linktitle: CharacterUnitFirstLineIndent
articleTitle: CharacterUnitFirstLineIndent
second_title: Aspose.Words pour .NET
description: Découvrez la propriété ParagraphFormat CharacterUnitFirstLineIndent pour personnaliser facilement la première ligne ou le retrait suspendu de votre document pour un aspect soigné.
type: docs
weight: 70
url: /fr/net/aspose.words/paragraphformat/characterunitfirstlineindent/
---
## ParagraphFormat.CharacterUnitFirstLineIndent property

Obtient ou définit la valeur (en caractères) du retrait de première ligne ou du retrait suspendu.

Utilisez des valeurs positives pour définir le retrait de la première ligne et des valeurs négatives pour définir le retrait suspendu.

```csharp
public double CharacterUnitFirstLineIndent { get; set; }
```

## Exemples

Montre comment modifier l'espacement et les retraits des paragraphes.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
ParagraphFormat format = doc.FirstSection.Body.FirstParagraph.ParagraphFormat;

// Vous trouverez ci-dessous cinq options d'espacement différentes, ainsi que les propriétés que leur configuration affecte indirectement.
// 1 - Retrait à gauche :
Assert.AreEqual(format.LeftIndent, 0.0d);

format.CharacterUnitLeftIndent = 10.0;

Assert.AreEqual(format.LeftIndent, 120.0d);

// 2 - Retrait à droite :
Assert.AreEqual(format.RightIndent, 0.0d); 

format.CharacterUnitRightIndent = -5.5;

Assert.AreEqual(format.RightIndent, -66.0d);

// 3 - Retrait suspendu :
Assert.AreEqual(format.FirstLineIndent, 0.0d);

format.CharacterUnitFirstLineIndent = 20.3;

Assert.AreEqual(format.FirstLineIndent, 243.59d, 0.1d);

// 4 - Interligne avant les paragraphes :
Assert.AreEqual(format.SpaceBefore, 0.0d);

format.LineUnitBefore = 5.1;

Assert.AreEqual(format.SpaceBefore, 61.1d, 0.1d);

// 5 - Interligne après les paragraphes :
Assert.AreEqual(format.SpaceAfter, 0.0d);

format.LineUnitAfter = 10.9;

Assert.AreEqual(format.SpaceAfter, 130.8d, 0.1d);

builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
builder.Write("测试文档测试文档测试文档测试文档测试文档测试文档测试文档测试文档测试" +
              "文档测试文档测试文档测试文档测试文档测试文档测试文档测试文档测试文档测试文档");
```

### Voir également

* class [ParagraphFormat](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
