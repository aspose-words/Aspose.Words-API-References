---
title: DocumentBuilder.InsertDocument
linktitle: InsertDocument
articleTitle: InsertDocument
second_title: Aspose.Words para .NET
description: Inserte documentos fácilmente en cualquier posición del cursor con el método InsertDocument de DocumentBuilder. ¡Optimice su flujo de trabajo y mejore su productividad!
type: docs
weight: 310
url: /es/net/aspose.words/documentbuilder/insertdocument/
---
## InsertDocument(*[Document](../../document/), [ImportFormatMode](../../importformatmode/)*) {#insertdocument}

Inserta un documento en la posición del cursor.

```csharp
public Node InsertDocument(Document srcDoc, ImportFormatMode importFormatMode)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| srcDoc | Document | Documento fuente para insertar. |
| importFormatMode | ImportFormatMode | Especifica cómo combinar el formato de estilo que entra en conflicto. |

### Valor_devuelto

Primer nodo del contenido insertado.

## Observaciones

Este método imita el comportamiento de MS Word, como si se presionara CTRL+'A' (seleccionar todo el contenido), luego CTRL+'C' (copiar lo seleccionado en el buffer) dentro de un documento y luego CTRL+'V' (insertar contenido desde el buffer) dentro de otro documento.

## Ejemplos

Muestra cómo insertar un documento en otro documento.

```csharp
Document doc = new Document(MyDir + "Document.docx");

DocumentBuilder builder = new DocumentBuilder(doc);
builder.MoveToDocumentEnd();
builder.InsertBreak(BreakType.PageBreak);

Document docToInsert = new Document(MyDir + "Formatted elements.docx");

builder.InsertDocument(docToInsert, ImportFormatMode.KeepSourceFormatting);
builder.Document.Save(ArtifactsDir + "DocumentBuilder.InsertDocument.docx");
```

### Ver también

* class [Node](../../node/)
* class [Document](../../document/)
* enum [ImportFormatMode](../../importformatmode/)
* class [DocumentBuilder](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)

---

## InsertDocument(*[Document](../../document/), [ImportFormatMode](../../importformatmode/), [ImportFormatOptions](../../importformatoptions/)*) {#insertdocument_1}

Inserta un documento en la posición del cursor.

```csharp
public Node InsertDocument(Document srcDoc, ImportFormatMode importFormatMode, 
    ImportFormatOptions importFormatOptions)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| srcDoc | Document | Documento fuente para insertar. |
| importFormatMode | ImportFormatMode | Especifica cómo combinar el formato de estilo que entra en conflicto. |
| importFormatOptions | ImportFormatOptions | Permite especificar opciones que afectan el formato de un documento de resultado. |

### Valor_devuelto

Primer nodo del contenido insertado.

## Observaciones

Este método imita el comportamiento de MS Word, como si se presionara CTRL+'A' (seleccionar todo el contenido), luego CTRL+'C' (copiar lo seleccionado en el buffer) dentro de un documento y luego CTRL+'V' (insertar contenido desde el buffer) dentro de otro documento.

## Ejemplos

Muestra cómo resolver estilos duplicados al insertar documentos.

```csharp
Document dstDoc = new Document();
DocumentBuilder builder = new DocumentBuilder(dstDoc);

Style myStyle = builder.Document.Styles.Add(StyleType.Paragraph, "MyStyle");
myStyle.Font.Size = 14;
myStyle.Font.Name = "Courier New";
myStyle.Font.Color = Color.Blue;

builder.ParagraphFormat.StyleName = myStyle.Name;
builder.Writeln("Hello world!");

// Clona el documento y edita el estilo "MyStyle" del clon, para que sea de un color diferente al del original.
// Si insertamos el clon en el documento original, los dos estilos con el mismo nombre provocarán un conflicto.
Document srcDoc = dstDoc.Clone();
srcDoc.Styles["MyStyle"].Font.Color = Color.Red;

// Cuando habilitamos SmartStyleBehavior y usamos el modo de formato de importación KeepSourceFormatting,
// Aspose.Words resolverá los conflictos de estilo convirtiendo los estilos del documento fuente.
// con los mismos nombres que los estilos de destino en atributos de párrafo directo.
ImportFormatOptions options = new ImportFormatOptions();
options.SmartStyleBehavior = true;

builder.InsertDocument(srcDoc, ImportFormatMode.KeepSourceFormatting, options);

dstDoc.Save(ArtifactsDir + "DocumentBuilder.SmartStyleBehavior.docx");
```

### Ver también

* class [Node](../../node/)
* class [Document](../../document/)
* enum [ImportFormatMode](../../importformatmode/)
* class [ImportFormatOptions](../../importformatoptions/)
* class [DocumentBuilder](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
