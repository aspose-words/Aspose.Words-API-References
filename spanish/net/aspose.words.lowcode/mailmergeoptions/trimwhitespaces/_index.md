---
title: MailMergeOptions.TrimWhitespaces
linktitle: TrimWhitespaces
articleTitle: TrimWhitespaces
second_title: Aspose.Words para .NET
description: Optimice la combinación de correspondencia con la propiedad TrimWhitespaces. Gestione fácilmente los espacios iniciales y finales para obtener documentos más limpios y profesionales.
type: docs
weight: 110
url: /es/net/aspose.words.lowcode/mailmergeoptions/trimwhitespaces/
---
## MailMergeOptions.TrimWhitespaces property

Obtiene o establece un valor que indica si los espacios iniciales y finales se eliminan de los valores de combinación de correspondencia.

```csharp
public bool TrimWhitespaces { get; set; }
```

## Observaciones

El valor predeterminado es`verdadero` .

## Ejemplos

Muestra cómo realizar la operación de combinación de correspondencia para un solo registro.

```csharp
// Hay varias formas de realizar la operación de combinación de correspondencia:
string doc = MyDir + "Mail merge.doc";

string[] fieldNames = new string[] { "FirstName", "Location", "SpecialCharsInName()" };
string[] fieldValues = new string[] { "James Bond", "London", "Classified" };

MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMerge.1.docx", fieldNames, fieldValues);
MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMerge.2.docx", SaveFormat.Docx, fieldNames, fieldValues);
MailMergeOptions mailMergeOptions = new MailMergeOptions();
mailMergeOptions.TrimWhitespaces = true;
MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMerge.3.docx", SaveFormat.Docx, fieldNames, fieldValues, mailMergeOptions);
```

### Ver también

* class [MailMergeOptions](../)
* espacio de nombres [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* asamblea [Aspose.Words](../../../)
