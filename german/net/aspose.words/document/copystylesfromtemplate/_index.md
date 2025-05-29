---
title: Document.CopyStylesFromTemplate
linktitle: CopyStylesFromTemplate
articleTitle: CopyStylesFromTemplate
second_title: Aspose.Words für .NET
description: Kopieren Sie mit der Methode „CopyStylesFromTemplate“ mühelos Stile aus der von Ihnen gewählten Vorlage in jedes beliebige Dokument und verbessern Sie so Ihren Arbeitsablauf und die Dokumentkonsistenz.
type: docs
weight: 610
url: /de/net/aspose.words/document/copystylesfromtemplate/
---
## CopyStylesFromTemplate(*string*) {#copystylesfromtemplate_1}

Kopiert Stile aus der angegebenen Vorlage in ein Dokument.

```csharp
public void CopyStylesFromTemplate(string template)
```

## Bemerkungen

Wenn Stile aus einer Vorlage in ein Dokument kopiert werden, werden gleichnamige Stile im Dokument neu definiert, sodass sie den Stilbeschreibungen in der Vorlage entsprechen. Eindeutige Stile aus der Vorlage werden in das Dokument kopiert. Eindeutige Stile im Dokument bleiben erhalten.

## Beispiele

Zeigt, wie Stile von einem Dokument in ein anderes kopiert werden.

```csharp
// Erstellen Sie ein Dokument und fügen Sie dann Stile hinzu, die wir in ein anderes Dokument kopieren.
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

// Erstellen Sie ein Dokument, in das wir die Stile kopieren.
Document target = new Document();

// Erstellen Sie einen Stil mit demselben Namen wie ein Stil aus dem Vorlagendokument und fügen Sie ihn dem Zieldokument hinzu.
style = target.Styles.Add(StyleType.Paragraph, "TemplateStyle3");
style.Font.Name = "Calibri";
style.Font.Color = Color.Orange;

Assert.AreEqual(5, target.Styles.Count);

// Es gibt zwei Möglichkeiten, die Methode aufzurufen, um alle Stile von einem Dokument in ein anderes zu kopieren.
// 1 - Übergabe des Vorlagendokumentobjekts:
target.CopyStylesFromTemplate(template);

// Durch das Kopieren von Stilen werden alle Stile aus dem Vorlagendokument zum Ziel hinzugefügt
// und überschreibt vorhandene Stile mit demselben Namen.
Assert.AreEqual(7, target.Styles.Count);

Assert.AreEqual("Courier New", target.Styles["TemplateStyle3"].Font.Name);
Assert.AreEqual(Color.RoyalBlue.ToArgb(), target.Styles["TemplateStyle3"].Font.Color.ToArgb());

// 2 - Übergeben des lokalen Systemdateinamens eines Vorlagendokuments:
target.CopyStylesFromTemplate(MyDir + "Rendering.docx");

Assert.AreEqual(21, target.Styles.Count);
```

### Siehe auch

* class [Document](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)

---

## CopyStylesFromTemplate(*[Document](../)*) {#copystylesfromtemplate}

Kopiert Stile aus der angegebenen Vorlage in ein Dokument.

```csharp
public void CopyStylesFromTemplate(Document template)
```

## Bemerkungen

Wenn Stile aus einer Vorlage in ein Dokument kopiert werden, werden gleichnamige Stile im Dokument neu definiert, sodass sie den Stilbeschreibungen in der Vorlage entsprechen. Eindeutige Stile aus der Vorlage werden in das Dokument kopiert. Eindeutige Stile im Dokument bleiben erhalten.

## Beispiele

Zeigt, wie Stile über „Dokument“ aus der Vorlage in ein Dokument kopiert werden.

```csharp
Document template = new Document(MyDir + "Rendering.docx");
Document target = new Document(MyDir + "Document.docx");

target.CopyStylesFromTemplate(template);
```

Zeigt, wie Stile von einem Dokument in ein anderes kopiert werden.

```csharp
// Erstellen Sie ein Dokument und fügen Sie dann Stile hinzu, die wir in ein anderes Dokument kopieren.
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

// Erstellen Sie ein Dokument, in das wir die Stile kopieren.
Document target = new Document();

// Erstellen Sie einen Stil mit demselben Namen wie ein Stil aus dem Vorlagendokument und fügen Sie ihn dem Zieldokument hinzu.
style = target.Styles.Add(StyleType.Paragraph, "TemplateStyle3");
style.Font.Name = "Calibri";
style.Font.Color = Color.Orange;

Assert.AreEqual(5, target.Styles.Count);

// Es gibt zwei Möglichkeiten, die Methode aufzurufen, um alle Stile von einem Dokument in ein anderes zu kopieren.
// 1 - Übergabe des Vorlagendokumentobjekts:
target.CopyStylesFromTemplate(template);

// Durch das Kopieren von Stilen werden alle Stile aus dem Vorlagendokument zum Ziel hinzugefügt
// und überschreibt vorhandene Stile mit demselben Namen.
Assert.AreEqual(7, target.Styles.Count);

Assert.AreEqual("Courier New", target.Styles["TemplateStyle3"].Font.Name);
Assert.AreEqual(Color.RoyalBlue.ToArgb(), target.Styles["TemplateStyle3"].Font.Color.ToArgb());

// 2 - Übergeben des lokalen Systemdateinamens eines Vorlagendokuments:
target.CopyStylesFromTemplate(MyDir + "Rendering.docx");

Assert.AreEqual(21, target.Styles.Count);
```

### Siehe auch

* class [Document](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
