---
title: ParagraphFormat.CharacterUnitRightIndent
linktitle: CharacterUnitRightIndent
articleTitle: CharacterUnitRightIndent
second_title: Aspose.Words pour .NET
description: Découvrez la propriété ParagraphFormat CharacterUnitRightIndent pour ajuster facilement les valeurs de retrait à droite des caractères de vos paragraphes, améliorant ainsi la mise en page de votre document.
type: docs
weight: 90
url: /fr/net/aspose.words/paragraphformat/characterunitrightindent/
---
## ParagraphFormat.CharacterUnitRightIndent property

Obtient ou définit la valeur de retrait correcte (en caractères) pour les paragraphes spécifiés.

```csharp
public double CharacterUnitRightIndent { get; set; }
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
