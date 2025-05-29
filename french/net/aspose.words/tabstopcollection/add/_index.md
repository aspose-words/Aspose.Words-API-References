---
title: TabStopCollection.Add
linktitle: Add
articleTitle: Add
second_title: Aspose.Words pour .NET
description: Découvrez comment la méthode TabStopCollection Add ajoute ou met à jour efficacement les taquets de tabulation, améliorant ainsi la mise en page et le formatage de votre document.
type: docs
weight: 30
url: /fr/net/aspose.words/tabstopcollection/add/
---
## Add(*[TabStop](../../tabstop/)*) {#add}

Ajoute ou remplace un taquet de tabulation dans la collection.

```csharp
public void Add(TabStop tabStop)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| tabStop | TabStop | Un objet tabulation à ajouter. |

## Remarques

Si un taquet de tabulation existe déjà à la position spécifiée, il est remplacé.

## Exemples

Montre comment ajouter des taquets de tabulation personnalisés à un document.

```csharp
Document doc = new Document();
Paragraph paragraph = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);

// Vous trouverez ci-dessous deux manières d'ajouter des taquets de tabulation à la collection de taquets de tabulation d'un paragraphe via la propriété « ParagraphFormat ».
// 1 - Créez un objet « TabStop », puis ajoutez-le à la collection :
TabStop tabStop = new TabStop(ConvertUtil.InchToPoint(3), TabAlignment.Left, TabLeader.Dashes);
paragraph.ParagraphFormat.TabStops.Add(tabStop);

// 2 - Transmettez les valeurs des propriétés d'un nouveau taquet de tabulation à la méthode « Add » :
paragraph.ParagraphFormat.TabStops.Add(ConvertUtil.MillimeterToPoint(100), TabAlignment.Left,
    TabLeader.Dashes);

// Ajouter des tabulations à 5 cm à tous les paragraphes.
foreach (Paragraph para in doc.GetChildNodes(NodeType.Paragraph, true).OfType<Paragraph>())
{
    para.ParagraphFormat.TabStops.Add(ConvertUtil.MillimeterToPoint(50), TabAlignment.Left,
        TabLeader.Dashes);
}

// Chaque caractère « tabulation » amène le curseur du constructeur à l'emplacement du prochain taquet de tabulation.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Start\tTab 1\tTab 2\tTab 3\tTab 4");

doc.Save(ArtifactsDir + "TabStopCollection.AddTabStops.docx");
```

### Voir également

* class [TabStop](../../tabstop/)
* class [TabStopCollection](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)

---

## Add(*double, [TabAlignment](../../tabalignment/), [TabLeader](../../tableader/)*) {#add_1}

Ajoute ou remplace un taquet de tabulation dans la collection.

```csharp
public void Add(double position, TabAlignment alignment, TabLeader leader)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| position | Double | Une position (en points) où ajouter le taquet de tabulation. |
| alignment | TabAlignment | UN[`TabAlignment`](../../tabalignment/) la valeur that spécifie l'alignement du texte au niveau de la tabulation. |
| leader | TabLeader | UN[`TabLeader`](../../tableader/)la valeur that spécifie le type de ligne de repère affichée sous le caractère de tabulation. |

## Remarques

Si un taquet de tabulation existe déjà à la position spécifiée, il est remplacé.

## Exemples

Montre comment ajouter des taquets de tabulation personnalisés à un document.

```csharp
Document doc = new Document();
Paragraph paragraph = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);

// Vous trouverez ci-dessous deux manières d'ajouter des taquets de tabulation à la collection de taquets de tabulation d'un paragraphe via la propriété « ParagraphFormat ».
// 1 - Créez un objet « TabStop », puis ajoutez-le à la collection :
TabStop tabStop = new TabStop(ConvertUtil.InchToPoint(3), TabAlignment.Left, TabLeader.Dashes);
paragraph.ParagraphFormat.TabStops.Add(tabStop);

// 2 - Transmettez les valeurs des propriétés d'un nouveau taquet de tabulation à la méthode « Add » :
paragraph.ParagraphFormat.TabStops.Add(ConvertUtil.MillimeterToPoint(100), TabAlignment.Left,
    TabLeader.Dashes);

// Ajouter des tabulations à 5 cm à tous les paragraphes.
foreach (Paragraph para in doc.GetChildNodes(NodeType.Paragraph, true).OfType<Paragraph>())
{
    para.ParagraphFormat.TabStops.Add(ConvertUtil.MillimeterToPoint(50), TabAlignment.Left,
        TabLeader.Dashes);
}

// Chaque caractère « tabulation » amène le curseur du constructeur à l'emplacement du prochain taquet de tabulation.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Start\tTab 1\tTab 2\tTab 3\tTab 4");

doc.Save(ArtifactsDir + "TabStopCollection.AddTabStops.docx");
```

### Voir également

* enum [TabAlignment](../../tabalignment/)
* enum [TabLeader](../../tableader/)
* class [TabStopCollection](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
