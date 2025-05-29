---
title: Document.CopyStylesFromTemplate
linktitle: CopyStylesFromTemplate
articleTitle: CopyStylesFromTemplate
second_title: Aspose.Words för .NET
description: Kopiera enkelt stilar från din valda mall till valfritt dokument med metoden CopyStylesFromTemplate, vilket förbättrar ditt arbetsflöde och dokumentkonsekvens.
type: docs
weight: 610
url: /sv/net/aspose.words/document/copystylesfromtemplate/
---
## CopyStylesFromTemplate(*string*) {#copystylesfromtemplate_1}

Kopierar stilar från den angivna mallen till ett dokument.

```csharp
public void CopyStylesFromTemplate(string template)
```

## Anmärkningar

När stilar kopieras från en mall till ett dokument, omdefinieras stilar med liknande namn i dokumentet för att matcha stilbeskrivningarna i mallen. Unika stilar från mallen kopieras till dokumentet. Unika stilar i dokumentet förblir intakta.

## Exempel

Visar hur man kopierar stilar från ett dokument till ett annat.

```csharp
// Skapa ett dokument och lägg sedan till stilar som vi ska kopiera till ett annat dokument.
Document template = new Document();

Style style = template.Styles.Add(StyleType.Paragraph, "TemplateStyle1");
style.Font.Name = "Times New Roman";
style.Font.Color = Color.Navy;

style = template.Styles.Add(StyleType.Paragraph, "TemplateStyle2");
style.Font.Name = "Arial";
style.Font.Color = Color.DeepSkyBlue;

style = template.Styles.Add(StyleType.Paragraph, "TemplateStyle3");
style.Font.Name = "Courier New";
style.Font.Color = Color.RoyalBlue;

Assert.AreEqual(7, template.Styles.Count);

// Skapa ett dokument som vi ska kopiera stilarna till.
Document target = new Document();

// Skapa en stil med samma namn som en stil från malldokumentet och lägg till den i måldokumentet.
style = target.Styles.Add(StyleType.Paragraph, "TemplateStyle3");
style.Font.Name = "Calibri";
style.Font.Color = Color.Orange;

Assert.AreEqual(5, target.Styles.Count);

// Det finns två sätt att anropa metoden för att kopiera alla stilar från ett dokument till ett annat.
// 1 - Skicka malldokumentobjektet:
target.CopyStylesFromTemplate(template);

// Kopiering av stilar lägger till alla stilar från malldokumentet till måldokumentet
// och skriver över befintliga stilar med samma namn.
Assert.AreEqual(7, target.Styles.Count);

Assert.AreEqual("Courier New", target.Styles["TemplateStyle3"].Font.Name);
Assert.AreEqual(Color.RoyalBlue.ToArgb(), target.Styles["TemplateStyle3"].Font.Color.ToArgb());

// 2 - Skicka det lokala systemfilnamnet för ett malldokument:
target.CopyStylesFromTemplate(MyDir + "Rendering.docx");

Assert.AreEqual(21, target.Styles.Count);
```

### Se även

* class [Document](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)

---

## CopyStylesFromTemplate(*[Document](../)*) {#copystylesfromtemplate}

Kopierar stilar från den angivna mallen till ett dokument.

```csharp
public void CopyStylesFromTemplate(Document template)
```

## Anmärkningar

När stilar kopieras från en mall till ett dokument, omdefinieras stilar med liknande namn i dokumentet för att matcha stilbeskrivningarna i mallen. Unika stilar från mallen kopieras till dokumentet. Unika stilar i dokumentet förblir intakta.

## Exempel

Visar hur man kopierar stilar från mallen till ett dokument via Dokument.

```csharp
Document template = new Document(MyDir + "Rendering.docx");
Document target = new Document(MyDir + "Document.docx");

target.CopyStylesFromTemplate(template);
```

Visar hur man kopierar stilar från ett dokument till ett annat.

```csharp
// Skapa ett dokument och lägg sedan till stilar som vi ska kopiera till ett annat dokument.
Document template = new Document();

Style style = template.Styles.Add(StyleType.Paragraph, "TemplateStyle1");
style.Font.Name = "Times New Roman";
style.Font.Color = Color.Navy;

style = template.Styles.Add(StyleType.Paragraph, "TemplateStyle2");
style.Font.Name = "Arial";
style.Font.Color = Color.DeepSkyBlue;

style = template.Styles.Add(StyleType.Paragraph, "TemplateStyle3");
style.Font.Name = "Courier New";
style.Font.Color = Color.RoyalBlue;

Assert.AreEqual(7, template.Styles.Count);

// Skapa ett dokument som vi ska kopiera stilarna till.
Document target = new Document();

// Skapa en stil med samma namn som en stil från malldokumentet och lägg till den i måldokumentet.
style = target.Styles.Add(StyleType.Paragraph, "TemplateStyle3");
style.Font.Name = "Calibri";
style.Font.Color = Color.Orange;

Assert.AreEqual(5, target.Styles.Count);

// Det finns två sätt att anropa metoden för att kopiera alla stilar från ett dokument till ett annat.
// 1 - Skicka malldokumentobjektet:
target.CopyStylesFromTemplate(template);

// Kopiering av stilar lägger till alla stilar från malldokumentet till måldokumentet
// och skriver över befintliga stilar med samma namn.
Assert.AreEqual(7, target.Styles.Count);

Assert.AreEqual("Courier New", target.Styles["TemplateStyle3"].Font.Name);
Assert.AreEqual(Color.RoyalBlue.ToArgb(), target.Styles["TemplateStyle3"].Font.Color.ToArgb());

// 2 - Skicka det lokala systemfilnamnet för ett malldokument:
target.CopyStylesFromTemplate(MyDir + "Rendering.docx");

Assert.AreEqual(21, target.Styles.Count);
```

### Se även

* class [Document](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
