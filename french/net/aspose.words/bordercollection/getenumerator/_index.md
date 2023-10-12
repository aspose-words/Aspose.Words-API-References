---
title: BorderCollection.GetEnumerator
second_title: Référence de l'API Aspose.Words pour .NET
description: BorderCollection méthode. Renvoie un objet énumérateur qui peut être utilisé pour parcourir toutes les bordures de la collection.
type: docs
weight: 160
url: /fr/net/aspose.words/bordercollection/getenumerator/
---
## BorderCollection.GetEnumerator method

Renvoie un objet énumérateur qui peut être utilisé pour parcourir toutes les bordures de la collection.

```csharp
public IEnumerator<Border> GetEnumerator()
```

### Exemples

Montre comment parcourir et modifier toutes les bordures d’un objet au format paragraphe.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Configurez les paramètres de format de paragraphe du générateur pour créer une bordure de vague verte de tous les côtés.
BorderCollection borders = builder.ParagraphFormat.Borders;

using (IEnumerator<Border> enumerator = borders.GetEnumerator())
{
    while (enumerator.MoveNext())
    {
        Border border = enumerator.Current;
        border.Color = Color.Green;
        border.LineStyle = LineStyle.Wave;
        border.LineWidth = 3;
    }
}

// Insère un paragraphe. Nos paramètres de bordure détermineront l'apparence de sa bordure.
builder.Writeln("Hello world!");

doc.Save(ArtifactsDir + "BorderCollection.GetBordersEnumerator.docx");
```

### Voir également

* class [Border](../../border/)
* class [BorderCollection](../)
* espace de noms [Aspose.Words](../../bordercollection/)
* Assemblée [Aspose.Words](../../../)


