---
title: Document.AppendDocument
linktitle: AppendDocument
articleTitle: AppendDocument
second_title: Aspose.Words para .NET
description: Adjunte documentos fácilmente con nuestro método "Anexar Documentos". Mejore su flujo de trabajo integrando contenido a la perfección en sus archivos existentes.
type: docs
weight: 570
url: /es/net/aspose.words/document/appenddocument/
---
## AppendDocument(*[Document](../), [ImportFormatMode](../../importformatmode/)*) {#appenddocument}

Agrega el documento especificado al final de este documento.

```csharp
public void AppendDocument(Document srcDoc, ImportFormatMode importFormatMode)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| srcDoc | Document | El documento a adjuntar. |
| importFormatMode | ImportFormatMode | Especifica cómo combinar el formato de estilo que entra en conflicto. |

## Ejemplos

Muestra cómo agregar un documento al final de otro documento.

```csharp
Document srcDoc = new Document();
srcDoc.FirstSection.Body.AppendParagraph("Source document text. ");

Document dstDoc = new Document();
dstDoc.FirstSection.Body.AppendParagraph("Destination document text. ");

// Anexa el documento de origen al documento de destino conservando su formato.
// luego guarde el documento fuente en el sistema de archivos local.
dstDoc.AppendDocument(srcDoc, ImportFormatMode.KeepSourceFormatting);
dstDoc.Save(ArtifactsDir + "Document.AppendDocument.docx");
```

Muestra cómo agregar todos los documentos de una carpeta al final de un documento de plantilla.

```csharp
Document dstDoc = new Document();

DocumentBuilder builder = new DocumentBuilder(dstDoc);
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Writeln("Template Document");
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Normal;
builder.Writeln("Some content here");
// Adjunte todos los documentos no cifrados con la extensión .doc
// desde nuestro directorio de sistema de archivos local al documento base.
List<string> docFiles = Directory.GetFiles(MyDir, "*.doc").Where(item => item.EndsWith(".doc")).ToList();
foreach (string fileName in docFiles)
{
    FileFormatInfo info = FileFormatUtil.DetectFileFormat(fileName);
    if (info.IsEncrypted)
        continue;

    Document srcDoc = new Document(fileName);
    dstDoc.AppendDocument(srcDoc, ImportFormatMode.UseDestinationStyles);
}

dstDoc.Save(ArtifactsDir + "Document.AppendAllDocumentsInFolder.doc");
```

### Ver también

* enum [ImportFormatMode](../../importformatmode/)
* class [Document](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)

---

## AppendDocument(*[Document](../), [ImportFormatMode](../../importformatmode/), [ImportFormatOptions](../../importformatoptions/)*) {#appenddocument_1}

Agrega el documento especificado al final de este documento.

```csharp
public void AppendDocument(Document srcDoc, ImportFormatMode importFormatMode, 
    ImportFormatOptions importFormatOptions)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| srcDoc | Document | El documento a adjuntar. |
| importFormatMode | ImportFormatMode | Especifica cómo combinar el formato de estilo que entra en conflicto. |
| importFormatOptions | ImportFormatOptions | Permite especificar opciones que afectan el formato de un documento de resultado. |

## Ejemplos

Muestra cómo gestionar conflictos en el estilo de lista al agregar un clon de un documento a sí mismo.

```csharp
Document srcDoc = new Document(MyDir + "List item.docx");
Document dstDoc = new Document(MyDir + "List item.docx");

// Si hay un conflicto de estilos de lista, aplique el formato de lista del documento de origen.
// Establezca la propiedad "KeepSourceNumbering" en "falso" para no importar ningún número de lista al documento de destino.
// Establezca la propiedad "KeepSourceNumbering" en "verdadero" e importe todos los conflictos
// estilo de lista de numeración con la misma apariencia que tenía en el documento fuente.
DocumentBuilder builder = new DocumentBuilder(dstDoc);
builder.MoveToDocumentEnd();
builder.InsertBreak(BreakType.SectionBreakNewPage);

ImportFormatOptions options = new ImportFormatOptions();
options.KeepSourceNumbering = keepSourceNumbering;
builder.InsertDocument(srcDoc, ImportFormatMode.KeepSourceFormatting, options);

dstDoc.UpdateListLabels();
```

Muestra cómo gestionar conflictos en el estilo de lista al insertar un documento.

```csharp
Document dstDoc = new Document();
DocumentBuilder builder = new DocumentBuilder(dstDoc);
builder.InsertBreak(BreakType.ParagraphBreak);

dstDoc.Lists.Add(ListTemplate.NumberDefault);
Aspose.Words.Lists.List list = dstDoc.Lists[0];

builder.ListFormat.List = list;

for (int i = 1; i <= 15; i++)
    builder.Write($"List Item {i}\n");

Document attachDoc = (Document)dstDoc.Clone(true);

// Si hay un conflicto de estilos de lista, aplique el formato de lista del documento de origen.
// Establezca la propiedad "KeepSourceNumbering" en "falso" para no importar ningún número de lista al documento de destino.
// Establezca la propiedad "KeepSourceNumbering" en "verdadero" e importe todos los conflictos
// estilo de lista de numeración con la misma apariencia que tenía en el documento fuente.
ImportFormatOptions importOptions = new ImportFormatOptions();
importOptions.KeepSourceNumbering = keepSourceNumbering;

builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.InsertDocument(attachDoc, ImportFormatMode.KeepSourceFormatting, importOptions);

dstDoc.Save(ArtifactsDir + "DocumentBuilder.InsertDocumentAndResolveStyles.docx");
```

Muestra cómo gestionar conflictos en el estilo de lista al agregar un documento.

```csharp
//Cargue un documento con texto en un estilo personalizado y clónelo.
Document srcDoc = new Document(MyDir + "Custom list numbering.docx");
Document dstDoc = srcDoc.Clone();

//Ahora tenemos dos documentos, cada uno con un estilo idéntico llamado "CustomStyle".
// Cambia el color del texto de uno de los estilos para diferenciarlo del otro.
dstDoc.Styles["CustomStyle"].Font.Color = Color.DarkRed;

// Si hay un conflicto de estilos de lista, aplique el formato de lista del documento de origen.
// Establezca la propiedad "KeepSourceNumbering" en "falso" para no importar ningún número de lista al documento de destino.
// Establezca la propiedad "KeepSourceNumbering" en "verdadero" e importe todos los conflictos
// estilo de lista de numeración con la misma apariencia que tenía en el documento fuente.
ImportFormatOptions options = new ImportFormatOptions();
options.KeepSourceNumbering = keepSourceNumbering;

// Unir dos documentos que tienen estilos diferentes y que comparten el mismo nombre provoca un conflicto de estilos.
//Podemos especificar un modo de formato de importación al agregar documentos para resolver este conflicto.
dstDoc.AppendDocument(srcDoc, ImportFormatMode.KeepDifferentStyles, options);
dstDoc.UpdateListLabels();

dstDoc.Save(ArtifactsDir + "DocumentBuilder.AppendDocumentAndResolveStyles.docx");
```

### Ver también

* enum [ImportFormatMode](../../importformatmode/)
* class [ImportFormatOptions](../../importformatoptions/)
* class [Document](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
