---
title: XpsSaveOptions
linktitle: XpsSaveOptions
articleTitle: XpsSaveOptions
second_title: Aspose.Words pour .NET
description: Découvrez le constructeur XpsSaveOptions pour créer sans effort des instances pour enregistrer des documents au format XPS, améliorant ainsi l'efficacité de votre gestion de documents.
type: docs
weight: 10
url: /fr/net/aspose.words.saving/xpssaveoptions/xpssaveoptions/
---
## XpsSaveOptions() {#constructor}

Initialise une nouvelle instance de cette classe qui peut être utilisée pour enregistrer un document dans leXps format.

```csharp
public XpsSaveOptions()
```

## Exemples

Montre comment limiter le niveau des titres qui apparaîtront dans le plan d'un document XPS enregistré.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insérer des titres pouvant servir d'entrées de table des matières de niveaux 1, 2, puis 3.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;

Assert.True(builder.ParagraphFormat.IsHeading);

builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;

builder.Writeln("Heading 1.1");
builder.Writeln("Heading 1.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading3;

builder.Writeln("Heading 1.2.1");
builder.Writeln("Heading 1.2.2");

// Créez un objet « XpsSaveOptions » que nous pouvons transmettre à la méthode « Save » du document
// pour modifier la façon dont cette méthode convertit le document en .XPS.
XpsSaveOptions saveOptions = new XpsSaveOptions();

Assert.AreEqual(SaveFormat.Xps, saveOptions.SaveFormat);

// Le document XPS de sortie contiendra un plan, une table des matières qui répertorie les titres dans le corps du document.
// Cliquer sur une entrée dans ce plan nous amènera à l'emplacement de son titre respectif.
// Définissez la propriété « HeadingsOutlineLevels » sur « 2 » pour exclure tous les titres dont les niveaux sont supérieurs à 2 du plan.
// Les deux derniers titres que nous avons insérés ci-dessus n'apparaîtront pas.
saveOptions.OutlineOptions.HeadingsOutlineLevels = 2;

doc.Save(ArtifactsDir + "XpsSaveOptions.OutlineLevels.xps", saveOptions);
```

### Voir également

* class [XpsSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)

---

## XpsSaveOptions(*[SaveFormat](../../../aspose.words/saveformat/)*) {#constructor_1}

Initialise une nouvelle instance de cette classe qui peut être utilisée pour enregistrer un document dans leXps ouOpenXps format.

```csharp
public XpsSaveOptions(SaveFormat saveFormat)
```

## Exemples

Montre comment enregistrer un document au format XPS sous la forme d'un pli de livre.

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");

// Créez un objet « XpsSaveOptions » que nous pouvons transmettre à la méthode « Save » du document
// pour modifier la façon dont cette méthode convertit le document en .XPS.
XpsSaveOptions xpsOptions = new XpsSaveOptions(SaveFormat.Xps);

// Définissez la propriété « UseBookFoldPrintingSettings » sur « true » pour organiser le contenu
// dans le XPS de sortie d'une manière qui nous aide à l'utiliser pour créer un livret.
// Définissez la propriété « UseBookFoldPrintingSettings » sur « false » pour restituer le XPS normalement.
xpsOptions.UseBookFoldPrintingSettings = renderTextAsBookFold;

// Si nous rendons le document sous forme de livret, nous devons définir les « MultiplePages »
// propriétés des objets de mise en page de toutes les sections sur « MultiplePagesType.BookFoldPrinting ».
if (renderTextAsBookFold)
    foreach (Section s in doc.Sections)
    {
        s.PageSetup.MultiplePages = MultiplePagesType.BookFoldPrinting;
    }

// Une fois ce document imprimé, nous pouvons le transformer en livret en empilant les pages
// pour sortir de l'imprimante et plier au milieu.
doc.Save(ArtifactsDir + "XpsSaveOptions.BookFold.xps", xpsOptions);
```

### Voir également

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [XpsSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
