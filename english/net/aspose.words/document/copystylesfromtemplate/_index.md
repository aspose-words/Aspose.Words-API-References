---
title: Document.CopyStylesFromTemplate
linktitle: CopyStylesFromTemplate
articleTitle: CopyStylesFromTemplate
second_title: Aspose.Words for .NET
description: Effortlessly copy styles from your chosen template to any document with the CopyStylesFromTemplate method, enhancing your workflow and document consistency.
type: docs
weight: 610
url: /net/aspose.words/document/copystylesfromtemplate/
---
## CopyStylesFromTemplate(*string*) {#copystylesfromtemplate_1}

Copies styles from the specified template to a document.

```csharp
public void CopyStylesFromTemplate(string template)
```

## Remarks

When styles are copied from a template to a document, like-named styles in the document are redefined to match the style descriptions in the template. Unique styles from the template are copied to the document. Unique styles in the document remain intact.

## Examples

Shows how to copy styles from one document to another.

```csharp
// Create a document, and then add styles that we will copy to another document.
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

Assert.That(template.Styles.Count, Is.EqualTo(7));

// Create a document which we will copy the styles to.
Document target = new Document();

// Create a style with the same name as a style from the template document and add it to the target document.
style = target.Styles.Add(StyleType.Paragraph, "TemplateStyle3");
style.Font.Name = "Calibri";
style.Font.Color = Color.Orange;

Assert.That(target.Styles.Count, Is.EqualTo(5));

// There are two ways of calling the method to copy all the styles from one document to another.
// 1 -  Passing the template document object:
target.CopyStylesFromTemplate(template);

// Copying styles adds all styles from the template document to the target
// and overwrites existing styles with the same name.
Assert.That(target.Styles.Count, Is.EqualTo(7));

Assert.That(target.Styles["TemplateStyle3"].Font.Name, Is.EqualTo("Courier New"));
Assert.That(target.Styles["TemplateStyle3"].Font.Color.ToArgb(), Is.EqualTo(Color.RoyalBlue.ToArgb()));

// 2 -  Passing the local system filename of a template document:
target.CopyStylesFromTemplate(MyDir + "Rendering.docx");

Assert.That(target.Styles.Count, Is.EqualTo(21));
```

### See Also

* class [Document](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)

---

## CopyStylesFromTemplate(*[Document](../)*) {#copystylesfromtemplate}

Copies styles from the specified template to a document.

```csharp
public void CopyStylesFromTemplate(Document template)
```

## Remarks

When styles are copied from a template to a document, like-named styles in the document are redefined to match the style descriptions in the template. Unique styles from the template are copied to the document. Unique styles in the document remain intact.

## Examples

Shows how to copies styles from the template to a document via Document.

```csharp
Document template = new Document(MyDir + "Rendering.docx");
Document target = new Document(MyDir + "Document.docx");

target.CopyStylesFromTemplate(template);
```

Shows how to copy styles from one document to another.

```csharp
// Create a document, and then add styles that we will copy to another document.
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

Assert.That(template.Styles.Count, Is.EqualTo(7));

// Create a document which we will copy the styles to.
Document target = new Document();

// Create a style with the same name as a style from the template document and add it to the target document.
style = target.Styles.Add(StyleType.Paragraph, "TemplateStyle3");
style.Font.Name = "Calibri";
style.Font.Color = Color.Orange;

Assert.That(target.Styles.Count, Is.EqualTo(5));

// There are two ways of calling the method to copy all the styles from one document to another.
// 1 -  Passing the template document object:
target.CopyStylesFromTemplate(template);

// Copying styles adds all styles from the template document to the target
// and overwrites existing styles with the same name.
Assert.That(target.Styles.Count, Is.EqualTo(7));

Assert.That(target.Styles["TemplateStyle3"].Font.Name, Is.EqualTo("Courier New"));
Assert.That(target.Styles["TemplateStyle3"].Font.Color.ToArgb(), Is.EqualTo(Color.RoyalBlue.ToArgb()));

// 2 -  Passing the local system filename of a template document:
target.CopyStylesFromTemplate(MyDir + "Rendering.docx");

Assert.That(target.Styles.Count, Is.EqualTo(21));
```

### See Also

* class [Document](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
