---
title: Document.CopyStylesFromTemplate
linktitle: CopyStylesFromTemplate
articleTitle: CopyStylesFromTemplate
second_title: Aspose.Words para .NET
description: Copie sin esfuerzo estilos de su plantilla elegida a cualquier documento con el método CopyStylesFromTemplate, mejorando su flujo de trabajo y la consistencia del documento.
type: docs
weight: 610
url: /es/net/aspose.words/document/copystylesfromtemplate/
---
## CopyStylesFromTemplate(*string*) {#copystylesfromtemplate_1}

Copia estilos de la plantilla especificada a un documento.

```csharp
public void CopyStylesFromTemplate(string template)
```

## Observaciones

Al copiar estilos de una plantilla a un documento, los estilos con nombres similares en el documento se redefinen para que coincidan con las descripciones de la plantilla. Los estilos únicos de la plantilla se copian al documento. Los estilos únicos del documento se conservan.

## Ejemplos

Muestra cómo copiar estilos de un documento a otro.

```csharp
// Crea un documento y luego agrega estilos que copiaremos a otro documento.
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

// Crea un documento al que copiaremos los estilos.
Document target = new Document();

// Cree un estilo con el mismo nombre que un estilo del documento de plantilla y agréguelo al documento de destino.
style = target.Styles.Add(StyleType.Paragraph, "TemplateStyle3");
style.Font.Name = "Calibri";
style.Font.Color = Color.Orange;

Assert.AreEqual(5, target.Styles.Count);

// Hay dos formas de llamar al método para copiar todos los estilos de un documento a otro.
// 1 - Pasando el objeto de documento de plantilla:
target.CopyStylesFromTemplate(template);

// Copiar estilos agrega todos los estilos del documento de plantilla al destino
// y sobrescribe los estilos existentes con el mismo nombre.
Assert.AreEqual(7, target.Styles.Count);

Assert.AreEqual("Courier New", target.Styles["TemplateStyle3"].Font.Name);
Assert.AreEqual(Color.RoyalBlue.ToArgb(), target.Styles["TemplateStyle3"].Font.Color.ToArgb());

// 2 - Pasar el nombre de archivo del sistema local de un documento de plantilla:
target.CopyStylesFromTemplate(MyDir + "Rendering.docx");

Assert.AreEqual(21, target.Styles.Count);
```

### Ver también

* class [Document](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)

---

## CopyStylesFromTemplate(*[Document](../)*) {#copystylesfromtemplate}

Copia estilos de la plantilla especificada a un documento.

```csharp
public void CopyStylesFromTemplate(Document template)
```

## Observaciones

Al copiar estilos de una plantilla a un documento, los estilos con nombres similares en el documento se redefinen para que coincidan con las descripciones de la plantilla. Los estilos únicos de la plantilla se copian al documento. Los estilos únicos del documento se conservan.

## Ejemplos

Muestra cómo copiar estilos de la plantilla a un documento a través de Documento.

```csharp
Document template = new Document(MyDir + "Rendering.docx");
Document target = new Document(MyDir + "Document.docx");

target.CopyStylesFromTemplate(template);
```

Muestra cómo copiar estilos de un documento a otro.

```csharp
// Crea un documento y luego agrega estilos que copiaremos a otro documento.
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

// Crea un documento al que copiaremos los estilos.
Document target = new Document();

// Cree un estilo con el mismo nombre que un estilo del documento de plantilla y agréguelo al documento de destino.
style = target.Styles.Add(StyleType.Paragraph, "TemplateStyle3");
style.Font.Name = "Calibri";
style.Font.Color = Color.Orange;

Assert.AreEqual(5, target.Styles.Count);

// Hay dos formas de llamar al método para copiar todos los estilos de un documento a otro.
// 1 - Pasando el objeto de documento de plantilla:
target.CopyStylesFromTemplate(template);

// Copiar estilos agrega todos los estilos del documento de plantilla al destino
// y sobrescribe los estilos existentes con el mismo nombre.
Assert.AreEqual(7, target.Styles.Count);

Assert.AreEqual("Courier New", target.Styles["TemplateStyle3"].Font.Name);
Assert.AreEqual(Color.RoyalBlue.ToArgb(), target.Styles["TemplateStyle3"].Font.Color.ToArgb());

// 2 - Pasar el nombre de archivo del sistema local de un documento de plantilla:
target.CopyStylesFromTemplate(MyDir + "Rendering.docx");

Assert.AreEqual(21, target.Styles.Count);
```

### Ver también

* class [Document](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
