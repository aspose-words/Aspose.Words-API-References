---
title: MailMerge.CleanupParagraphsWithPunctuationMarks
linktitle: CleanupParagraphsWithPunctuationMarks
articleTitle: CleanupParagraphsWithPunctuationMarks
second_title: Aspose.Words para .NET
description: MailMerge CleanupParagraphsWithPunctuationMarks propiedad. Obtiene o establece un valor que indica si los párrafos con signos de puntuación se consideran vacíos y deben eliminarse si elRemoveEmptyParagraphs se especifica la opción en C#.
type: docs
weight: 20
url: /es/net/aspose.words.mailmerging/mailmerge/cleanupparagraphswithpunctuationmarks/
---
## MailMerge.CleanupParagraphsWithPunctuationMarks property

Obtiene o establece un valor que indica si los párrafos con signos de puntuación se consideran vacíos y deben eliminarse si elRemoveEmptyParagraphs se especifica la opción.

```csharp
public bool CleanupParagraphsWithPunctuationMarks { get; set; }
```

## Observaciones

El valor predeterminado es`verdadero` .

Aquí está la lista completa de signos de puntuación que se pueden limpiar:

* !
* ,
* .
* :
* ;
* ?
* ¡
* ¿

## Ejemplos

Muestra cómo eliminar párrafos con signos de puntuación después de una operación de combinación de correspondencia.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldMergeField mergeFieldOption1 = (FieldMergeField) builder.InsertField("MERGEFIELD", "Option_1");
mergeFieldOption1.FieldName = "Option_1";

builder.Write(punctuationMark);

FieldMergeField mergeFieldOption2 = (FieldMergeField) builder.InsertField("MERGEFIELD", "Option_2");
mergeFieldOption2.FieldName = "Option_2";

// Configure la propiedad "CleanupOptions" para eliminar los párrafos vacíos que crearía esta combinación de correspondencia.
doc.MailMerge.CleanupOptions = MailMergeCleanupOptions.RemoveEmptyParagraphs;

// Establecer la propiedad "CleanupParagraphsWithPunctuationMarks" en "true" también contará los párrafos
// con signos de puntuación vacíos y obtendrá la operación de combinación de correspondencia para eliminarlos también.
// Establecer la propiedad "CleanupParagraphsWithPunctuationMarks" en "false"
// eliminará los párrafos vacíos, pero no los que tengan signos de puntuación.
// Esta es una lista de signos de puntuación a los que se refiere esta propiedad: "!", ",", ".", ":", ";", "?", "¡", "¿".
doc.MailMerge.CleanupParagraphsWithPunctuationMarks = cleanupParagraphsWithPunctuationMarks;

doc.MailMerge.Execute(new[] { "Option_1", "Option_2" }, new object[] { null, null });

doc.Save(ArtifactsDir + "MailMerge.RemoveColonBetweenEmptyMergeFields.docx");
```

### Ver también

* class [MailMerge](../)
* espacio de nombres [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* asamblea [Aspose.Words](../../../)
